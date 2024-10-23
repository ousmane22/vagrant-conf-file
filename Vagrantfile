Vagrant.configure("2") do |config|
  
  config.vm.define "webserver" do |webserver|
    webserver.vm.box = "ubuntu/trusty64"
    webserver.vm.box_check_update = false
    webserver.vm.network "forwarded_port", guest: 80, host: 82
    webserver.vm.network "private_network", ip: "192.168.33.10"
    webserver.vm.synced_folder "./web", "/var/www/html"

    webserver.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.cpus = 1
      vb.name = "webserver"
      vb.memory = "1024"
    end
  end
end
