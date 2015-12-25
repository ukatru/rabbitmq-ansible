Vagrant.configure("2") do |config|
#  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.define "rmq001" do |rmq001|
  rmq001.vm.box = "rmq001"
  rmq001.vm.box_url = "/home/ukatru/vagrant/is115/centos-6-7-x64-is-virtualbox.box"
  rmq001.vm.hostname = "rmq001"
  rmq001.vm.network :public_network, bridge: "p2p1" ,ip: "192.168.2.117"
  #talend.timezone.value = "US/Pacific"
  rmq001.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
  #  vb.gui = true
  #
  #   # Customize the amount of memory on the VM:
          vb.name = "rmq001"
     vb.memory = "4196"
  end
  config.vm.provision "ansible" do |ansible|
   ansible.playbook = "rabbitmq.yml"
   #ansible.inventory_path = "hosts"
  end

end

end
