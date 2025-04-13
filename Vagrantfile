Vagrant.configure("2") do |config|
    # Указываем ОС, версию, количество ядер и ОЗУ
    config.vm.box = "centos/stream9"
    config.vm.box_version = "20250331.0"
 
    config.vm.provider :virtualbox do |v|
      v.memory = 2048
      v.cpus = 1
    end
  
    # Указываем имена хостов и их IP-адреса
    boxes = [
      { :name => "ipa.otus.lan",
        :ip => "192.168.56.10",
      },
      { :name => "client1.otus.lan",
        :ip => "192.168.56.11",
      },
      { :name => "client2.otus.lan",
        :ip => "192.168.56.12",
      }
    ]
    # Цикл запуска виртуальных машин
    boxes.each do |opts|
      config.vm.define opts[:name] do |config|
        config.vm.hostname = opts[:name]
        config.vm.network "private_network", ip: opts[:ip]
        config.vm.synced_folder "vmshare/", "/vagrant"
      end
    end
  end
