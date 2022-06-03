## Full Stack Web Development Environments
Need a full stack web development environment on your MacOs, linux, or Windows machine? AracPac's got you covered with 
out-of-the-box support for a variety of full stack web development frameworks, including:
* ✅ LAMP: Laravel / Symfony / CakePHP / CodeIgnitor
* ✅ JS: Angular / Ember / Express / Vue / React
* ✅ Java Spring
* ✅ Ruby on Rails
* ✅ Django
* ✅ ASP.Net

Check the latest releases on [https://app.vagrantup.com/aracpac/](https://app.vagrantup.com/aracpac/) for comprehensive notes on the current configurations.

## Usage
* install [vagrant](https://www.vagrantup.com/docs/installation) and [virtualbox](https://www.virtualbox.org/wiki/Downloads)
* download an AracPac Vagrantfile to an empty directory:
  * [Ubuntu 22.04 LTS](https://raw.githubusercontent.com/aracpac/aracpac-vagrantfiles/master/ubuntu22/Vagrantfile)
  * [CentOs 9 Stream](https://raw.githubusercontent.com/aracpac/aracpac-vagrantfiles/master/centos9-stream/Vagrantfile)
* navigate to the directory and `vagrant up`
* access the box at [https://dev.local/](https://dev.local/)

## Advanced usage: images built from sources
To modify the build and create an image catered to your needs:
* install [packer](https://www.packer.io/docs/install), [ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html), and [virtualbox](https://www.virtualbox.org/wiki/Downloads)
* clone the packer repository: `git clone https://github.com/aracpac/aracpac-packer-builds`
* modify the packer, shell, or ansible configuration files
* build a box: `cd centos8-stream && packer build packer.json`
* once the build is complete, your image will be in the `./builds` directory. you can now add it to your local vagrant 
collection `vagrant box add centos8-stream-v1.4.0 builds/centos8-v1.4.0.box` or upload it to https://app.vagrantup.com/
and share it with the world.
