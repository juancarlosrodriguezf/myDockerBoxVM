# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrant config
Vagrant.configure("2") do |config|
  config.vm.box      = "williamyeh/ubuntu-trusty64-docker"
  config.vm.hostname = "myDockerBox"
  config.vm.define     "myDockerBoxVM"
  
  # Check for updates only on `vagrant box outdated`
  config.vm.box_check_update = false

  config.vm.provider "virtualbox" do |vb|
    vb.name   = "MyDockerBox"
    vb.memory = "4096" # 4 GB
  end

  config.vm.provision "shell", path: "scripts/add_docker.sh"
end
