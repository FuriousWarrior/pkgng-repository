# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "uchida/poudriere"
  config.vm.provider "virtualbox" do |vb|
    vb.cpus = 1
    vb.memory = 2048
    #vb.gui = true
  end
  config.ssh.shell = "/bin/sh"
  config.vm.synced_folder ".", "/vagrant", type: 'rsync'

  config.vm.provision "shell", path: "provision.sh"
end
