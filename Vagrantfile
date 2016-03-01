# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure('2') do |config|
  config.vm.box      = 'ubuntu/trusty64'
  config.vm.hostname = 'rails-dev-box'
  config.vm.provision :shell, path: 'bootstrap.sh', keep_color: true
  
  config.vm.network "private_network", type: "dhcp"

  ## feel free modify it base on your computer
  config.vm.provider "virtualbox" do |v|
    v.memory = 2024
  end

  ## This is for linux and Mac users only. See more (http://docs.vagrantup.com/v2/synced-folders/nfs.html)
  ## '~' mean it will add all your directory of current user. Feel free for modify
  config.vm.synced_folder "~", "/vagrant", :nfs => true
end