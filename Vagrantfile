# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-20.04"
  
  config.vm.network "private_network", ip: "192.168.44.40"
  config.vm.network "forwarded_port", guest: 22, host: 6077, id: "ssh"
  config.vm.network "forwarded_port", guest: 3306, host: 4450, id: "mysql"
  
  config.vm.provider "virtualbox" do |v|
	v.name = "ubuntu_20_build_0001"
	v.memory = 4096
	v.cpus = 1
   end

  # Enable provisioning with a shell script. Additional provisioners such as
  # Ansible, Chef, Docker, Puppet and Salt are also available. Please see the
  # documentation for more information about their specific syntax and use.
   config.vm.provision "shell", path: "bootstrap.sh"
end