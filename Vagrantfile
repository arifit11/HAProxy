# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://atlas.hashicorp.com/search.
  # haproxy configuration
  config.vm.define "haproxy" do |haproxy|
    haproxy.vm.box = "centos/7"
    haproxy.vm.network "private_network", ip: "192.168.33.10"
    haproxy.vm.network "public_network", bridge: "en0: Wi-Fi (AirPort)"
    #haproxy.ssh.username = "vagrant"
    #haproxy.ssh.password = "vagrant"
    config.vm.provider "virtualbox" do |haproxy|
      haproxy.memory = 1024
      haproxy.cpus = 1
    end
    config.vm.provision "shell", inline: <<-SHELL
       yum update all
       #yum install -y python
     SHELL
  end
  # web_server1 configuration
  config.vm.define "web_server1" do |web_server1|
    web_server1.vm.box = "centos/7"
    web_server1.vm.network "private_network", ip: "192.168.33.11"
    web_server1.vm.network "public_network", bridge: "en0: Wi-Fi (AirPort)"
    #test_box.ssh.username = "vagrant"
    #test_box.ssh.password = "vagrant"
    config.vm.provider "virtualbox" do |web_server1|
      web_server1.memory = 1024
      web_server1.cpus = 1
    end
    config.vm.provision "shell", inline: <<-SHELL
       yum update all
       #yum install -y python
     SHELL
  end

  # web_server2 configuration
  config.vm.define "web_server2" do |web_server2|
    web_server2.vm.box = "centos/7"
    web_server2.vm.network "private_network", ip: "192.168.33.12"
    web_server2.vm.network "public_network", bridge: "en0: Wi-Fi (AirPort)"
    #test_box.ssh.username = "vagrant"
    #test_box.ssh.password = "vagrant"
    config.vm.provider "virtualbox" do |web_server2|
      web_server2.memory = 1014
      web_server2.cpus = 1
    end
    config.vm.provision "shell", inline: <<-SHELL
       yum update all
      #yum install -y python
     SHELL
  end
end
