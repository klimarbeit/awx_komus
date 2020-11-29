# AWX Repository

This one repository is dedicated to playbooks that are running with using of AWX (Ansible Tower) on infinity loop basis.

* **playbook** - directory contains specific playbooks  
  * **nginx** - execute nginx specific playbook that apply **nginx** role  
  * **docker** - execute docker engine specific playbook that apply **docker** role
  
* **roles** - directory contains ansible roles  
  * **nginx** - [ensures that installed on remote hosts](roles/nginx/README.md)  
  * **docker** - [ensures that installed on remote hosts](roles/docker/README.md)  
  