Vagrant.configure("2") do |config|
  config.vm.provision "shell", inline: "echo Hello"

  config.vm.define "web" do |web|
    web.vm.box = "spox/ubuntu-arm" 
    web.vm.box_version = "1.0.0"
    web.vm.network "private_network", ip: "192.168.56.17"
    web.vm.network "public_network"
  end

  config.vm.define "db" do |db|
    db.vm.box = "jacobw/fedora35-arm64"
    db.vm.network "private_network", ip: "192.168.56.15"
    db.vm.network "public_network"
  end
end
