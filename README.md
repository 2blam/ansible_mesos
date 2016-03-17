## Ansible Script for setting up mesos cluster

This script will set up a cluster with 4 machines:

1 master node - 192.168.199.10

2 slave nodes - 192.168.199.11,  192.168.199.12

1 data node - 192.168.199.13


Mesos master node will connect to 2 slaves.

Each salve can access the data node volume (data_volume) by using glusterfs.

## How to run this script


1) edit the inventory and provide the correct user, password and sudo password. [I assumed all hosts with the same login and password]

2) Command: ansible-playbook playbook.yml

## Note:
1) The script did not install mesos-dns 