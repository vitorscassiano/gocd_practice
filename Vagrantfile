# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANT_VERSION = "2"

Vagrant.configure(VAGRANT_VERSION) do |config|
  config.vm.define :server do |gocd|
    gocd.vm.box = "centos/7"
    gocd.vm.network :private_network, ip: "192.168.1.10"
    gocd.vm.provision "ansible" do |ansible|
      ansible.playbook = "ansible/gocd.yml"
    end
  end

  config.vm.define :agent1 do |gocd|
    gocd.vm.box = "centos/7"
    gocd.vm.network :private_network, ip: "192.168.1.12"
    gocd.vm.provision "ansible" do |ansible|
      ansible.playbook = "ansible/gocd.yml"
    end
  end

  config.vm.define :agent2 do |gocd|
    gocd.vm.box = "centos/7"
    gocd.vm.network :private_network, ip: "192.168.1.14"
    gocd.vm.provision "ansible" do |ansible|
      ansible.playbook = "ansible/gocd.yml"
    end
  end
end
