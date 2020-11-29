# Docker role

This role ensures that Docker CE service is installed in proper configuration

## Tasks

* **check_data_drive** - ensures that Docker data drive is locate on different drive then root partition, otherwise fails role applying  
* **add_repository** - installs official Docker CE repository  
* **service_installed** - installs Docker CE in latest stable version if not  
* **service_enabled** - enables Docker as service if not  
* **service_configuration** - installs proper NGINX server configuration and Service will be reloaded on changes  
* **service_started** - ensures that Docker service is restarted  

## Variables

* **docker.config.path** - path to Docker service configuration data  
* **docker.config.components** - the list of packages required by Docker CE engine  
* **docker.config.data.path** - path to Docker service data  
* **docker.config.log.type** - type of Docker engine logging driver (allowed types: *syslog*, *fluentd*, *gelf*)  
* **docker.config.log.protocol** - protocol that will be use by Docker logging driver
* **docker.config.log.address** - aggregation Service address where to logs would be sent by logging driver  
* **docker.config.log.port** - listening port of aggregation Service  

## Handlers

* **reload docker** - reloads Docker service on configuration changes  

## Templates

* **docker.json** - template of Docker service configuration, with enabling of live-restore, metrics and overlay2 as storage driver option  

[Back to TOC](../../README.md)