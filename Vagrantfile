# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
    config.vm.box = "sudishrestha/bahmni92"
    config.vm.box_check_update = true
    config.ssh.insert_key = false
    config.vm.network "private_network", ip: "192.168.33.10"
  
    config.vm.synced_folder "..", "/bahmni", :owner => "vagrant"
    config.vm.provider "virtualbox" do |v|
       v.customize ["modifyvm", :id, "--memory", 3092, "--cpus", 2, "--name", "Bahmni-RPM"]
    end
  end