# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
  config.vm.define "centos7" do |db|
    db.vm.box = "centos/7"
    db.vm.hostname = 'centos7'
    db.vm.box_url = "centos/7"
    end
  config.vm.define "bionic64" do |web|
    web.vm.box = "ubuntu/bionic64"
    web.vm.hostname = 'bionic64'
    web.vm.network "forwarded_port", guest: 80, host: 8080
    web.vm.box_url = "ubuntu/bionic64" 
    web.vm.provision "shell", inline: <<-SHELL
sudo apt update
sudo apt install -y apache2
SHELL
   end
end
