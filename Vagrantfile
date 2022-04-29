Vagrant.configure("2") do |config|
  config.vm.define :haproxyVm do |haproxyVm|
    haproxyVm.vm.box = "bento/ubuntu-20.04"
    haproxyVm.vm.network :private_network, ip: "192.168.56.30"
    haproxyVm.vm.provision "shell", path: "haproxyfolder/script.sh"
    haproxyVm.vm.hostname = "haproxyVm"
  end
  config.vm.define :web1 do |web1|
    web1.vm.box = "bento/ubuntu-20.04"
    web1.vm.network :private_network, ip: "192.168.56.31"
    web1.vm.provision "shell", path: "web1folder/script.sh"
    web1.vm.hostname = "web1"
  end
  config.vm.define :web2 do |web2|
   web2.vm.box = "bento/ubuntu-20.04"
   web2.vm.network :private_network, ip: "192.168.56.32"
   web2.vm.provision "shell", path: "web2folder/script.sh"
   web2.vm.hostname = "web2"
  end
end