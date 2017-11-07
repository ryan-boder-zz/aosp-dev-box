# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-16.04"

  config.vm.provider "virtualbox" do |vb|
    vb.gui = true
    # vb.memory = "1024"
  end

  config.vm.provision "shell", inline: <<-SHELL
    cd /vagrant/provision
    apt-get update
    ./install-packages
    ./android-ndk
    ./auto-gui
    ./auto-login
  SHELL
end
