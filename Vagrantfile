# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "bento/centos-6.7"
  config.vm.box_version = "2.2.5"
  
  config.vm.network "private_network", ip: "192.168.33.10"

  #config.vm.provider "virtualbox" do |vb|
  #  vb.gui = true
  #  vb.memory = "1024"
  #end

  config.vm.provision "shell", inline: <<-SHELL
    sudo yum update
    sudo yum install -y httpd
    sudo /etc/init.d/httpd start
  SHELL
end
