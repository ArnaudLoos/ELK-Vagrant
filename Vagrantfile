# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.define "elasticsearch" do |machine|

    machine.vm.provider "virtualbox" do |v|
      v.name = "Test-Elasticsearch"    #The name as shown in virtualbox console
      v.memory = 4096
      v.cpus   = 4
    end

    machine.vm.box = "ubuntu/bionic64"
    machine.vm.hostname = "elasticsearch"      #Change the hostname inside the OS
    machine.vm.network "public_network", bridge: "enp24s0"   #Bridge a nic onto my network

    # Provision with Ansible
    machine.vm.provision "ansible" do |ansible|
      ansible.playbook = "./ELK_setup.yml"
    end
  end
end









