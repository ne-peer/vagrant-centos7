# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.ssh.insert_key = false
  config.vm.network "forwarded_port", guest: 22, host: 2222, id: "ssh"
  config.vm.network "forwarded_port", guest: 80, host: 8888
  config.vm.synced_folder "./data", "/vagrant", type: "virtualbox"
  config.vm.provider "virtualbox" do |vb|
    vb.gui = false
    vb.memory = "1024"
  end
  config.vm.provision "shell", path: './provision_root.sh'
  config.vm.provision "shell", path: './provision_root_vi.sh'
  config.vm.provision :reload
end