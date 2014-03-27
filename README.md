Ansible Galera Cluster Install Playbook
---------------------------------------

This is the server-install Ansible playbook repository.

Requirements
------------

Not a lot here as most of the functionality is found in the ansible-galera playbook which has it's repo at https://github.com/CaptTofu/ansible-galera. This is specifically an Ansible Galaxy role you can install. The goal of galaxy is to make it so there is code re-use and you don't have to write your own

To install the Galaxy ansible-galera role:

    $ ansible-galaxy install username.rolename

Next, you will need to make sure you have a hosts file in the root directory of this repository or make sure to put in a [galera_cluster] group in your top-level ansible hosts. 

There is an example file, ``hosts.example`` if you want to roll your own. This can be used if instead of using the docker-galera repo to generate the hosts file, you instead simply add the IP addresses of the instances you wish to provision. You will need 4 instances and they will have to be set up with an SSH key that is also been added from where you are running ansible (with ``ssh-add``, provided ssh-agent is set up). If you can ssh as ubuntu@host without a password, then you are set.

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
