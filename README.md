# vagrant

There is a Vagrantfile and a Puppet configuration file to prepare the development environment.

____________________________________________________________________________________________________________

Example based on ubuntu 16.04/xenial arch.

Software requirements:
1. Git
2. VirtualBox
3. Vagrant

____________________________________________________________________________________________________________

Configuration:
1. Git installation
2. VirtualBox installation
3. Vagrant installation
4. Clone git repo
5. Deploy a VM

1.) Git installation

 #sudo apt-get install git

2.) VirtualBox installation

 #wget http://download.virtualbox.org/virtualbox/5.1.30/virtualbox-5.1_5.1.30-118389~Ubuntu~xenial_amd64.deb
 
 #sudo dpkg -i virtualbox-5.1_5.1.30-118389~Ubuntu~xenial_amd64.deb

3.) Vagrant installation

 #wget --no-check-certificate https://releases.hashicorp.com/vagrant/2.0.0/vagrant_2.0.0_x86_64.deb
 
 #sudo dpkg -i vagrant_2.0.0_x86_64.deb
        Install a plugin for sync via NFS support
        
 #vagrant plugin install vagrant-bindfs

    Vagrant HELP:
    # vagrant up (1-st time create and configure VM. 2-nd: start VM)
    # vagrant provision (update VM)
    # vagrant halt (shutdown VM)
    # vagrant destroy (remove VM)

4.) Copying files or clone git repo

 #mkdir ~/zaproo-centos-01
 
 #cd ~/zaproo-centos-01
 
 #git clone https://github.com/yagodin-pro/vagrant.git

5.) Start a VM creation process

 #cd ~/zaproo-centos-01/vagrant
 
 #vagrant up
