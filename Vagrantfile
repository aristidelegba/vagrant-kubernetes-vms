Vagrant.configure("2") do |config|
    config.ssh.insert_key = false
    config.vm.define "master" do |master|
      master.vm.box = "ubuntu/bionic64"
      master.vm.network "private_network", ip: "192.168.56.80"
    end
    config.vm.define "worker" do |worker|
      worker.vm.box = "ubuntu/bionic64"
      worker.vm.network "private_network", ip: "192.168.56.81"
    end
    config.vm.provider "virtualbox" do |vb|
      vb.memory = "3072"
      vb.cpus = "3"
    end
  end
