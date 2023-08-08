# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.

  Vagrant.configure("2") do |config|
      config.vm.define "jenkins" do |jenkins|
        jenkins.vm.box = "debian/bullseye64"
        jenkins.vm.provision "shell", inline: <<-SHELL
        sudo useradd -m -s /bin/bash -p 'ansible_webserver' ansible
        sudo usermod -aG sudo ansible
        echo 'Match User ansible' | sudo tee -a /etc/ssh/sshd_config
        echo '    PasswordAuthentication yes' | sudo tee -a /etc/ssh/sshd_config
        echo '    PubkeyAuthentication no' | sudo tee -a /etc/ssh/sshd_config
        sudo service ssh restart
        SHELL
      end
      
    
  end

