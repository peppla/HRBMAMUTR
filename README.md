# HRBMAMUTR
Vagrant lab to implement Heterogeneous Replication between MySQL and MongoDB using Tungsten Replicator

## Requirements
Vagrant

VirtualBox

[Vagrant VirtualBox VbGuest plugin](https://github.com/dotless-de/vagrant-vbguest)

Hostonly network configured for the network 192.168.56.0

## Install
Download files

Execute `vagrant up`

## Contents

* `Vagrantfile` (Vagrant vm configuration)
* `inventory` (ansible inventory file)
* `ansible.cfg` (ansible configuration)
* `mysql.yml` and `mongodb.yml` (playbooks to configure vm's)
* `tungsten.ini.mongodb` and `tungsten.ini.mysql` (tungsten configuration files for each node)

## Disclaimer
Some security features are disabled

Trivial or null passwords

Do not use with sensitive data or production environments
