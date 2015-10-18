# coding: utf-8
# -*- mode: ruby -*-

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/vivid64"
  # vboxsfがこわれないための対策
  config.vbguest.auto_update = false
  config.vm.network "private_network", ip: "10.20.30.40"
  config.vm.provider "virtualbox" do |vb|
    # Customize the amount of memory on the VM:
    vb.memory = "1024"
  end

  # Enable provisioning with a shell script. Additional provisioners such as
  # Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  # documentation for more information about their specific syntax and use.
  config.vm.provision "shell", inline: <<-SHELL
    /vagrant/build.sh
  SHELL
end
