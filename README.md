Ansible Galera Cluster Install Playbook
---------------------------------------

This is the server-install Ansible playbook repository.

Requirements
------------

Not a lot here as most of the functionality is found in the ansible-galera playbook which has it's repo at https://github.com/CaptTofu/ansible-galera. This is specifically an Ansible Galaxy role you can install. The goal of galaxy is to make it so there is code re-use and you don't have to write your own

To install the Galaxy ansible-galera role:

    $ ansible-galaxy install username.rolename

Next, you will need to make sure you have a hosts file in the root directory of this repository or make sure to put in a [galera_cluster] group in your top-level ansible hosts 

There is also a sample ansible-config file you can use if you don't want to have to edit /etc/ansible/ansible.cfg 

Role Variables
--------------

In ansible-galera

Dependencies
------------

ansible-galera
docker-galera (if using docker)

License
-------

Apache 2.0

Author Information
------------------

Patrick "CaptTofu" Galbraith <patg@hp.com> <patg@patg.net>
