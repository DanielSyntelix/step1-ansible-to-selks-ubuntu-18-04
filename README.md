# step1-ansible-to-selks-ubuntu-18-04
1st step to get SELKS

We're going to need to install Ansible and make an automation installation
ELK-SIEM-Ansible-Playbook
Ansible Playbook to install the ELK Stack. To use this playbook follow these steps:

Requirements:

Ansible on a VM or docker container.

Ubuntu VM for installing the ELK SIEM.

For a sample lab deployment, see mine here( and follow the whole series where i show you how to deploy ELK SIEM lab for detection): https://www.youtube.com/watch?v=IwlV3wVX4xs&t=32s

NB we will improve this playbook in the future to include roles and variables, for now lets keep it simple and use the site.yml.

#################

Install ansible on Centos 7 using install_ansible.sh

Clone this repo to your centos machine where you want to install Ansible
RUN cd ELK-SIEM-Ansible-playbook
run sudo ./install_ansible.sh ## This will install the latest version for ansible for you. For more info about this script, please go to: https://github.com/neillturner/omnibus-ansible
###############

Install ELK SIEM using Ansible

Clone this repo into your /etc/ansible folder
change the ip addresses from 192.168.5.71 to your SIEM IP addresses in the site.yml file
Run the Playbook site.yml ( ansible-playbook site.yml) ## This will take a while, get a coffee.
Sign into kibana at http://yoursiemip:5601 6)Next, get some data in your siem.
CREDITS: For the ansible install script: https://github.com/neillturner/omnibus-ansible
