<<<<<<< HEAD
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
    vb.memory = 1024
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
=======
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
    vb.memory = 1024
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
>>>>>>> a1a5e8259dd9b9edecf9de6b0cc2315257806f0a
