# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/trusty64"

  config.vm.network "private_network", ip: "192.168.50.4"

  config.vm.provider "virtualbox" do |vb|
    # Customize the amount of memory on the VM:
    vb.memory = "4096"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "fuse-ansible-openstack/bootstrap/site.yml"
    ansible.verbose = 'v'
  end

end