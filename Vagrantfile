# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

# $script = <<SCRIPT
# TODO: Put your install script here.
# SCRIPT

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # Box Settings
#  config.vm.box = "ubuntu/groovy64"
  config.vm.box = "bento/debian-11"

  # Provider Settings
  config.vm.provider "parallels" do |vb|
    vb.memory = 1024
  end

  # Network Settings
  config.vm.network "forwarded_port", guest:22, host: 2222

  config.vm.network "public_network", ip: "192.168.211.5", bridge: "AX88179A"
  # You can shell scripts when `vagrant up` or `vagrant provision` is run.
  # Just put scripts in the same directory as this `Vagrantfile`.
  #config.vm.provision "shell", privileged: false, path: "vagrant-bootstrap.sh"
  # You can do multiple scripts, if you want:
  #config.vm.provision "shell", privileged: false, path: "vagrant-bootstrap2.sh"
  #config.vm.provision "shell", privileged: true, inline: $script

  # Port forwarding examples
  # Just in case you need to run a database server, web server, etc.
  #config.vm.network "forwarded_port", guest: 8080, host: 8080
  #config.vm.network "forwarded_port", guest: 5000, host: 5000
  #config.vm.network "forwarded_port", guest: 35357, host: 35357

 

  # Shared folders:
  #
  # Setting the workspace to the current dir allows you to do editing/
  # development on host environment (OSX, etc.) and then actually run/
  # test things inside the virtual environvment.
  # You can map multiple folders in this way.
  # In this case, the ".", "/workspace" indicates that we want to map
  # the current directory on the host machine to the "/workspace" directory
  # on the guest/VM.
  #config.vm.synced_folder ".", "/proj"

end
