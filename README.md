# Playing with Ansible

*(NOT PRODUCTION WORTHY!)*

## Initialisation

This creates two Vagrant VMs - "controller" and "managed".

> cd vagrant  
> vagrant up  

### Controller
> This is our Ansible host  
> Shared folder: Host[/vagrant/share/controller]  
> SSH: 127.0.0.1:2200 (User: vagrant:vagrant)  
> Private network IP: 192.168.50.101  

### Managed
> This is the machine managed by the Ansible controller  
> Shared folder: Host[/vagrant/share/managed]  
> SSH: 127.0.0.1:2201 (User: vagrant:vagrant)  
> Private network IP: 192.168.50.102  

## Setup

SSH into the controller machine (with vagrant ssh controller, or using PuTTY)

> sudo apt-get update  
> sudo apt-get install python-software-properties  
> sudo apt-add-repository ppa:rquillo/ansible  
> sudo apt-get install ansible  
> sudo apt-get install sshpass  

> Copy / write:  
> files/etc-ansible-hosts to etc/ansible/hosts  

> Copy / write:  
> files/playbook1.yml to /home/vagrant/playbook1.yml  


## Run

> ansible-playbook /home/vagrant/playbook1.yml  
