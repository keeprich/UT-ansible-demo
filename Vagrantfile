# Author: Kenneth Dzonyrah
# Date: 02/01/2023
# Description: A simple vagrant file that will create servers to test ansible

# -*- mode: ruby -*- 
# vi: set ft=ruby : 
VAGRANTFILE_API_VERSION = "2" 
Vagrant.configure(VAGRANTFILE_API_VERSION) do|config| 
    config.ssh.insert_key = false 
    config.vm.provider :virtualbox do|vb| 
        vb.customize ["modifyvm", :id, "--memory", "2048"] 
    end 
    
    #Master server 
    config.vm.define "ansible-master" do|ansible| 
        ansible.vm.hostname = "master" 
        ansible.vm.box = "geerlingguy/centos7" 
        ansible.vm.network "private_network", ip: "192.168.56.150"

  end



   

    #------------------------------------- Install Ansible into the master server -----------------------

  
    #-----------------------------------------------------------------------------------------------------
    #Application Server1 
    config.vm.define "app1" do|app| 
        app.vm.hostname = "webserver" 
        app.vm.box = "geerlingguy/centos7" 
        app.vm.network "private_network", ip: "192.168.56.151" 
    end 
    
    
    #Database Server 
    config.vm.define "db" do|db| 
        db.vm.hostname = "database" 
        db.vm.box = "geerlingguy/centos7" 
        db.vm.network "private_network", ip: "192.168.56.152" 
    end 
    
    config.vm.box_check_update = false 
    #config.vbguest.auto_update = false 

  
      #......................................................................
end
    #..............................................................................
  




