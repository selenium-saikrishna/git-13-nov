# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
config.ssh.insert_key = false
config.vm.provider :virtualbox do |vb|
vb.customize ["modifyvm", :id, "--memory", "256"]
 end

 # control
 config.vm.define "Linux" do |app|
 app.vm.hostname = "Linux"
 app.vm.box = "ubuntu/trusty64"
 app.vm.network :private_network, ip: "192.168.60.1
 end
 

 end
