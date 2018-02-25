Vagrant.configure("2") do |config|

  config.vm.define "ansible" do |ansible|
    ansible.vm.box = "ubuntu/xenial64"
    ansible.vm.hostname = "ansible"
    ansible.vm.network "private_network", ip: "192.168.210.110"
    ansible.vm.synced_folder "ansible-example/", "/home/vagrant/ansible-example"
    ansible.vm.provision "shell", path: "setup.sh"
  end

  config.vm.define "host" do |host|
    host.vm.box = "bento/centos-7.2"
    host.vm.hostname = "host"
    host.vm.network "private_network", ip: "192.168.210.120"
  end
end
