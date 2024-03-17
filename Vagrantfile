# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    config.vm.provision "shell", inline: "echo Hello"
    
    config.vm.define "ubuntu" do |machine|
        machine.vm.provision "shell", path: "provision-ubuntu.sh"
        machine.vm.box = "ubuntu/trusty64"
        machine.vm.hostname = "ubuntu.local"
        machine.vm.network "private_network", ip: "192.168.0.2"
    end
    
    config.vm.define "centos" do |machine|
        machine.vm.provision "shell", path: "provision-centos.sh"
        machine.vm.box = "centos/7"
        machine.vm.hostname = "centos.local"
        machine.vm.network "private_network", ip: "192.168.0.3"
    end
end