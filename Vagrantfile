# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "srv01", primary: true do |srv|
      srv.vm.box = "bento/centos-7.4"
      srv.vm.hostname = "srv01"
      srv.vm.network "private_network", ip: "192.168.56.150"
      srv.vm.provider "virtualbox" do |vb|
          vb.memory = "1024"
          vb.cpus = "2"
      end
  end

  config.vm.define "srv02" do |srv|
      srv.vm.box = "bento/centos-7.4"
      srv.vm.hostname = "srv02"
      srv.vm.network "private_network", ip: "192.168.56.152"
      srv.vm.provider "virtualbox" do |vb|
          vb.memory = "512"
          vb.cpus = "1"
      end
  end

  config.vm.define "srv03" do |srv|
      srv.vm.box = "bento/centos-7.4"
      srv.vm.hostname = "srv03"
      srv.vm.network "private_network", ip: "192.168.56.153"
      srv.vm.provider "virtualbox" do |vb|
          vb.memory = "512"
          vb.cpus = "1"
      end
  end

  config.vm.provision "shell",  path: "swapfile.sh"
end
