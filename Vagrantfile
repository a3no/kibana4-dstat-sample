# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"
HOSTNAME1 = "kibana4-dstat-sample"
IP1 = "192.168.200.50"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "chef/centos-6.5"

  config.vm.define "#{HOSTNAME1}" do |guest|
    guest.vm.provision "shell", path: "ansible_local.sh"
    guest.vm.network :private_network, ip: IP1
    guest.vm.hostname = "#{HOSTNAME1}"
    guest.vm.provider "virtualbox" do |vb|
      vb.name = "#{HOSTNAME1}"
      vb.memory = 2048
    end
  end

end
