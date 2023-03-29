## Assignment 1

Create a Vagrantfile that provisions a VM with Apache installed and runs a simple Apache web page.
# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://vagrantcloud.com/search.
  config.vm.box = "bento/ubuntu-16.04"
    config.vm.network "private_network", ip: "192.168.33.10"
    config.vm.provision "shell", inline: <<-SHELL
      apt-get update
      apt-get install -y apache2
      service apache2 restart
      echo "this is web page" >> /var/www/html/index.html
    SHELL
end


## Assignment 2

Create a Vagrantfile that provisions a VM with Nginx installed and runs a simple Nginx web page.


## Assignment 3

Create a Vagrantfile that provisions a VM with MySQL installed and creates a database and a user.

## Assignment 4

Create a Vagrantfile that provisions a VM with MongoDB installed and creates a database and a user.

## Assignment 5

Create a Vagrantfile that provisions a VM with Node.js installed and runs a script.

## Assignment 6

Create a Vagrantfile that provisions a VM with Python installed and runs a script.

## Assignment 7

Create a Vagrantfile that provisions a VM with Ruby installed and runs a script.

## Assignment 8

Create a Vagrantfile that provisions a VM with Git installed and clones a repository.

## Assignment 9

Create a Vagrantfile that provisions a VM with Ansible installed and runs a playbook.
