# My Playbooks

A collection of minimalist Ansible playbooks for automating server setups

- [Initial Server Setup for Ubuntu 20.04](https://github.com/onovaes/ansible-playbooks/tree/master/initial_setup_ubuntu2004) *


*the Initial Server Setup should be your starting point for fresh servers.

Ansible >= 2.11.5 required


### Connection Test

From your local machine or Ansible control node, run:

```command
# Test with password and login
ansible all -m ping -u remote_user

# Test with ssk key
ansible all -m ping \
-u root \
--key-file=~/.ssh/id_rsa

```

If you're able to get a "pong" reply back from your node(s), your setup works as expected and you'll be able to run both ad-hoc commands and playbooks on your nodes, using Ansible.


### 1 - Clone
    
    $git clone git@github.com:onovaes/ansible-playbooks.git
    cd ansible-playbooks

### 2 - Conffile 
    
    $cp initial_setup_ubuntu2004/vars/example-default.yml initial_setup_ubuntu2004/vars/default.yml

### 3 - Run Playbook


    # RUN as root
    $ansible-playbook initial_setup_ubuntu2004/playbook.yml -u root 

    # RUN as otheruser with only called "dev" hosts group 
    $ansible-playbook initial_setup_ubuntu2004/playbook.yml -u otheruser -l dev --check --diff



## TODO's


[] Tirar inventario do playbook, pois devo passar como parametro no docker
[] validando instlaco do dockers
[] Acredito que não estava fazendo o upgrade inicial automatico

