Vagrant.configure("2") do |config|
 
  config.vm.box = "bento/ubuntu-16.04"
  config.vm.hostname = "cassandra"
  config.vm.network "private_network", ip: "192.168.33.10"
  config.vm.network "public_network", bridge: "en0"

  config.vm.provider "virtualbox" do |vb|
    # Display the VirtualBox GUI when booting the machine
    vb.name = "cassandra"
    vb.gui = false
    # Customize the amount of memory on the VM:
    vb.memory = "2048"
  end

  config.vm.provision "shell", path: "provision/default.sh", privileged: false
end
