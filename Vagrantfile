Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.hostname = "sloopstash-workstation"
  config.vm.box_check_update = false
  config.vm.network "private_network", ip: "192.168.99.100"
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.ssh.username = "vagrant"
  config.ssh.private_key_path=["~/.vagrant.d/insecure_private_key"]
  config.ssh.insert_key = false
  config.vm.provider "virtualbox" do |vb|
    vb.gui = false
    vb.memory = "1024"
    vb.cpus = "2"
    vb.name = "sloopstash-workstation"
  end
  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
  SHELL
end
