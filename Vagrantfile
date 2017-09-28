# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.define "mysql" do |mysql|
    mysql.vm.box = "centos/7"
    mysql.vm.network "private_network", ip: "192.168.56.210"

    mysql.vm.synced_folder ".", "/vagrant", type: "virtualbox", owner: "vagrant", mount_options: ["dmode=775,fmode=600"]
    mysql.vm.provision :ansible_local do |ansible|
      ansible.playbook = "mysql.yml"
      ansible.verbose = true
      ansible.install = true
      ansible.inventory_path = "inventory"
    end
  end
  config.vm.define "mongodb" do |mongodb|
    mongodb.vm.box = "centos/7"
    mongodb.vm.network "private_network", ip: "192.168.56.211"

    mongodb.vm.synced_folder ".", "/vagrant", type: "virtualbox", owner: "vagrant", mount_options: ["dmode=775,fmode=600"]

    mongodb.vm.provision :ansible_local do |ansible|
      ansible.playbook = "mongodb.yml"
      ansible.verbose = true
      ansible.install = true
      ansible.inventory_path = "inventory"
    end 
  end
  
end
