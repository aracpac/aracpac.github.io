# AracPac
Need a full stack web development environment on your MacOs, linux, or Windows machine? AracPac's got you covered:

## Basic usage: images hosted on Vagrant Cloud
* install [vagrant](https://www.vagrantup.com/docs/installation)
  * install vagrant plugins: `vagrant plugin install vagrant-hostmanager`
* install [virtualbox](https://www.virtualbox.org/wiki/Downloads)
* download an AracPac Vagrantfile to an empty directory:
  * [Ubuntu 20.04 LTS](https://raw.githubusercontent.com/aracpac/aracpac-vagrantfiles/master/ubuntu20/Vagrantfile)
  * [CentOs 8](https://raw.githubusercontent.com/aracpac/aracpac-vagrantfiles/master/ubuntu20/Vagrantfile)
* navigate to the directory and `vagrant up`
* access the box at https://dev.local/

## Advanced usage: images built from sources
To build a box from scratch:
* install [packer](https://www.packer.io/docs/install)
* install [ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)
* install [virtualbox](https://www.virtualbox.org/wiki/Downloads)
* clone the packer repository: `git clone https://github.com/aracpac/aracpac-packer-builds`
* build a box: `cd rhel8 && packer build packer.json`
* access built image in `./builds` directory 
