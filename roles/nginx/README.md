# NGINX role

This role assumes that all additional packages are pre-installed already.  
Logrotate, by example.

## Tasks

* **set_sysctl** - appies kernel settings optimized for NGINX hosting is applied and **sysctl** will be reloaded on changes  
* **add_repository** - installs official NGINX repository  
* **service_installed** - installs NGINX in defined version if not  
* **service_enabled** - enables NGINX as service if not  
* **service_logs** - ensures that directory for NGINX log files exist and has proper ACL applied  
* **service_configuration** - installs proper NGINX server configuration and Service will be reloaded on changes  
* **service_started** - ensures that NGINX service is started  
* **logrotate** - installs configuration for management of NGINX log files  

## Variables

* **nginx.version** - defines reuiqred version of NGINX to install  
* **nginx.log.path** - path to NGINX log files  
* **nginx.log.retention** - how many days keep archived log files  
* **nginx.pid.path** - path to PID file of NGINX  

## Handlers

* **reload nginx** - reloads NGINX configuration without reboot of Service  
* **reload updated sysctl** - reloads particular updated configuration of **sysctl**  

## Templates

* **logrotate** - template of logrotate configuration dedicated to NGINX log files  
* **nginx.conf** - template of NGINX main configuration  

## Files

* **nginx.repo** - official NGINX repository configuration file for CentOS 7  
* **sysctl-nginx.conf** - kernel settings optimized for hosts running NGINX server  

[Back to TOC](../../README.md)