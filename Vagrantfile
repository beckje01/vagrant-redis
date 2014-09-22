
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.network "forwarded_port", guest: 6379, host: 6379


  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/redis.yml"
    ansible.host_key_checking = false
  end
end
