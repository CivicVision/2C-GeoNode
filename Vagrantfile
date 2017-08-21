Vagrant.configure("2") do |config|

  #config.vm.network "private_network", ip: "192.168.33.10"
  config.vm.network "forwarded_port", guest: 8001, host: 8001
  config.vm.box = "ubuntu/xenial64"
  config.vm.synced_folder "state_2c_geonode/", "/home/ubuntu/state_2c_geonode/state_2c_geonode"
  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "playbook.local.yml"
  end
end
