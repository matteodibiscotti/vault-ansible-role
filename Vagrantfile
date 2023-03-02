# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  
  config.vm.define "ansible-controller" do |config|
    config.vm.box = "hashicorp/bionic64"
    config.vm.hostname = "ansiblecontroller"
    config.vm.network "private_network", ip: "10.1.42.101"
    config.vm.provision "shell", inline: "sudo apt update"
    config.vm.provision "shell", inline: "sudo apt install software-properties-common -y"
    config.vm.provision "shell", inline: "sudo add-apt-repository --yes --update ppa:ansible/ansible"
    config.vm.provision "shell", inline: "sudo apt install ansible -y"
    config.vm.provision "file", source: "C:\\Users\\ts-matthew.lowman\\ansible\\vault-deployment", destination: "/home/vagrant/vault-deployment"
  end

  config.vm.define "ansible-target1" do |config|
    config.vm.box = "hashicorp/bionic64"
    config.vm.hostname = "target1"
    config.vm.network "private_network", ip: "10.1.42.102"
    config.vm.provision "shell", inline: "sudo apt update"
    config.vm.provision "shell", inline: "sudo apt install software-properties-common -y"
    config.vm.provision "shell", inline: "sudo add-apt-repository --yes --update ppa:ansible/ansible"
    config.vm.provision "shell", inline: "sudo apt install ansible -y"
  end

  config.vm.define "ansible-target2" do |config|
    config.vm.box = "hashicorp/bionic64"
    config.vm.hostname = "target2"
    config.vm.network "private_network", ip: "10.1.42.103"
    config.vm.provision "shell", inline: "sudo apt update"
    config.vm.provision "shell", inline: "sudo apt install software-properties-common -y"
    config.vm.provision "shell", inline: "sudo add-apt-repository --yes --update ppa:ansible/ansible"
    config.vm.provision "shell", inline: "sudo apt install ansible -y"
  end

end