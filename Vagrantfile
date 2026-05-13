Vagrant.configure("2") do |config|
  config.vm.box = "generic/ubuntu2204-arm64"
  config.vm.hostname = "moodle-local"
  config.vm.network "private_network", ip: "192.168.56.20"
  config.vm.provider "virtualbox" do |vb|
    vb.name = "moodle-local"
    vb.memory = "4096"
    vb.cpus = 2
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end
end
