# -*- mode: ruby -*-
# vi: set ft=ruby :

DOMAIN = "local"
BOX = "leandrosolagna/centos"
BOX_VERSION = "0.0.1"

nodes = [
  {:hostname => "masternode", :ip => "192.168.56.2"},
  {:hostname => "workernode", :ip => "192.168.56.3"}
]

Vagrant.configure("2") do |config|

  nodes.each do |node|
    config.vm.define node[:hostname] do |nodeconfig|
      nodeconfig.vm.box = BOX
      nodeconfig.vm.box_version = BOX_VERSION
      nodeconfig.vm.hostname = node[:hostname] + DOMAIN
      nodeconfig.vm.network :private_network, ip: node[:ip]
      nodeconfig.vm.provider "virtualbox" do |vb|
        vb.cpus = "1"
        vb.memory = "1024"
      end
    end
  end
end #end of Vagrantfile
