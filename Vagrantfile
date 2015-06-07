# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  # Need this to set the name of the machine in vagrant's prompt
  config.vm.define "NatureByTheNumbers" do |naturebythenumbers|
    # This should be an arch linux box, with python2 already installed.
    naturebythenumbers.vm.box = "arch64"
    # This sets the name in the VirtualBox system and GUI, and gives us 1G of ram.
    naturebythenumbers.vm.provider "virtualbox" do |v|
      v.name = "NatureByTheNumbers"
      v.memory = 1024
    end

    # Forward to the port I will be using for jupyter
    naturebythenumbers.vm.network "forwarded_port", guest: 8000, host: 8000

    # Provision With Ansible
    naturebythenumbers.vm.provision "ansible" do |ansible|
      ansible.playbook = "provisioning/playbook.yaml"
      # This just lets me keep the server port in one place.
      ansible.extra_vars = {
        notebook_server_port: 8000
      }
    end
  end
end
