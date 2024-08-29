Vagrant.configure("2") do |config|

  # boxes at https://vagrantcloud.com/search.
  config.vm.box = "ubuntu/focal64"
  config.vm.box_version = "20240821.0.0" 
  # NOTE: This will enable public access to the opened port
  config.vm.network "forwarded_port", guest: 80, host: 8080

  #
   config.vm.provider "virtualbox" do |vb|
 
  #   # Customize the amount of memory on the VM:
     vb.memory = "2048"
     vb.cpus = "1"
    end
  
  # documentation for more information about their specific syntax and use.
   config.vm.provision "shell", inline: <<-SHELL
     apt-get update
     apt-get install -y apache2
   SHELL
end
