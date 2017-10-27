# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "pinx/CentOS-7-x86_64-1708"
  config.vm.box_version = "1.0"

  config.vm.host_name = "zaproo-centos-01"

  # config.vm.box_check_update = false

  config.vm.synced_folder "./data", "/home/web/public", nfs: true

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:
  #
  # config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
  #   vb.gui = true
  #
  #   # Customize the amount of memory on the VM:
  #   vb.memory = "1024"
  # end
  #

     config.vm.provision :puppet do |puppet|
          puppet.manifests_path = "puppet/manifests"
          puppet.module_path    = "puppet/modules"
          puppet.manifest_file  = "site.pp"
     end

end
