Ansible ELK Playbook
This playbook is for setting up version 5.x of the ELK Stack on a remote server.

Notes and requirements
The playbook was built and tested on Ubuntu 16.04 EC2, for ELK versions 5.x
You will need Ansible installed and running
Playbook is currently configured to set up the ELK stack together with Metricbeat for server perf monitoring. There is a role for Filebeat as well. You just need to add the Filebeat role to your site.yml file.
Instructions
Edit your Ansible hosts file ('/etc/ansible/hosts') and add an 'elkservers' entry for the server you wish to install ELK on. You can of course name the host any way you want, this is just an example.
Verify connectivity to the ELK server.
In the terminal on the machine hosting Ansible, clone this repo.
Cd into the directory, and run: ansible-playbook site.yml
The plays in the playbook will run on the target server, installing ELK and the specified beats shippers.
