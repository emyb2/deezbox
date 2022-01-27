Vagrant.configure("2") do |config|
  config.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--cpus", "3", "--memory", "4096"]
  end
  config.vm.box = "emy/deezbox"
  config.vm.hostname = "deezbox"
  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.network "private_network", ip: "192.168.33.10"
  config.vm.synced_folder ".", "/var/www", type: "nfs"
end
