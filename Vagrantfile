# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|

#artful does not work with defaults in vagrantcloud.com
 config.vm.define "control" do |ctl|
  ctl.vm.box = "ubuntu/trusty64"
  ctl.vm.hostname = "ubuntu-control"
  ctl.vm.network "private_network", ip: "192.168.56.102"
  ctl.vm.provider "virtualbox" do |vb|
    vb.memory = 4096
  end
 end

 #using https://github.com/ngaloha/ansible-confluent
 # and https://github.com/GlobalMaksimum/ansible-confluent-cluster
 #kafka confluent 1
 config.vm.define "kafka1" do |kaf01|
  kaf01.vm.box = "ubuntu/trusty64"
  kaf01.vm.hostname = "ubuntu-kafka1"
  kaf01.vm.network "private_network", ip: "192.168.56.104"
  kaf01.vm.synced_folder "../../Storage", "/vagrant_data"
  kaf01.vm.provider "virtualbox" do |vb|
    vb.memory = 4096
  end
 end

 #kafka confluent 2
 config.vm.define "kafka2" do |kaf02|
  kaf02.vm.box = "ubuntu/trusty64"
  kaf02.vm.hostname = "ubuntu-kafka2"
  kaf02.vm.network "private_network", ip: "192.168.56.105"
  kaf02.vm.synced_folder "../../Storage", "/vagrant_data"
  kaf02.vm.provider "virtualbox" do |vb| 
    vb.memory = 4096
   end
  end
  
  #kafka confluent 3
 config.vm.define "kafka3" do |kaf03|
  kaf03.vm.box = "ubuntu/trusty64"
  kaf03.vm.hostname = "ubuntu-kafka3"
  kaf03.vm.network "private_network", ip: "192.168.56.106"
  kaf03.vm.synced_folder "../../Storage", "/vagrant_data"
  kaf03.vm.provider "virtualbox" do |vb| 
    vb.memory = 4096
   end
  end
  
  # jptoto is a cloud image created by jptoto
 config.vm.define "webserver01" do |web01|
  web01.vm.box = "jptoto/Windows2012R2"
  web01.vm.hostname = "windows-webserver01"
  web01.vm.communicator = "winrm"
  web01.winrm.username  = "vagrant"
  web01.winrm.password  = "vagrant"
  web01.vm.network "private_network", ip: "192.168.56.103"
  web01.vm.provider "virtualbox" do |vb|
    vb.memory = 2048
    vb.cpus = 2
  end
 end
end
