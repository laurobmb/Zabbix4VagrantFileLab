Vagrant.configure("2") do |config|
  config.vm.define "zabbixS" do |zabbixS|
    zabbixS.vm.box = "bento/centos-7.3"
    zabbixS.vm.hostname = 'zabbixS.lab.zabbix.com'
    zabbixS.vm.box_url = "bento/centos-7.3"
    zabbixS.vm.network "forwarded_port", guest: 80, host: 8080
    zabbixS.vm.network :private_network, ip: "172.25.250.254"
    zabbixS.vm.network :public_network , bridge: "enp0s31f6"
    zabbixS.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 1048]
      v.customize ["modifyvm", :id, "--name", "zabbixS.lab.zabbix.com"]
      id_rsa_pub = File.read("#{Dir.home}/Dropbox/Chaves/Public-semsenha.openssh")
      config.vm.provision "copy ssh public key", type: "shell", inline: <<-SHELL
        echo #{id_rsa_pub} >> /home/vagrant/.ssh/authorized_keys
        mkdir /root/.ssh/
        touch /root/.ssh/authorized_keys
        echo #{id_rsa_pub} >> /root/.ssh/authorized_keys
        SHELL
  end
end  
# configurations of zabbixC1 machine
  config.vm.define "zabbixC1" do |zabbixC1|
    zabbixC1.vm.box = "bento/centos-7.3"
    zabbixC1.vm.hostname = 'zabbixC1.lab.zabbix.com'
    zabbixC1.vm.box_url = "bento/centos-7.3"
    zabbixC1.vm.network :private_network, ip: "172.25.250.252"
    zabbixC1.vm.network :public_network , bridge: "enp0s31f6"
    zabbixC1.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 1048]
      v.customize ["modifyvm", :id, "--name", "zabbixC1.lab.zabbix.com"]
      id_rsa_pub = File.read("#{Dir.home}/Dropbox/Chaves/Public-semsenha.openssh")
      config.vm.provision "copy ssh public key", type: "shell", inline: <<-SHELL
        echo #{id_rsa_pub} >> /home/vagrant/.ssh/authorized_keys
        mkdir /root/.ssh/
        touch /root/.ssh/authorized_keys
        echo #{id_rsa_pub} >> /root/.ssh/authorized_keys
        SHELL
  end
 end
 # configurations of zabbixP machine
  config.vm.define "zabbixP" do |zabbixP|
    zabbixP.vm.box = "bento/centos-7.3"
    zabbixP.vm.hostname = 'zabbixP.lab.zabbix.com'
    zabbixP.vm.box_url = "bento/centos-7.3"
    zabbixP.vm.network :private_network, ip: "172.25.250.253"
    zabbixP.vm.network :public_network , bridge: "enp0s31f6"
    zabbixP.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 1048]
      v.customize ["modifyvm", :id, "--name", "zabbixP.lab.zabbix.com"]
      id_rsa_pub = File.read("#{Dir.home}/Dropbox/Chaves/Public-semsenha.openssh")
      config.vm.provision "copy ssh public key", type: "shell", inline: <<-SHELL
        echo #{id_rsa_pub} >> /home/vagrant/.ssh/authorized_keys
        mkdir /root/.ssh/
        touch /root/.ssh/authorized_keys
        echo #{id_rsa_pub} >> /root/.ssh/authorized_keys
        SHELL
  end
 end
 # configurations of zabbixC2 machine
  config.vm.define "zabbixC2" do |zabbixC2|
    zabbixC2.vm.box = "centos/6"
    zabbixC2.vm.hostname = 'zabbixC2.lab.zabbix.com'
    zabbixC2.vm.box_url = "centos/6"
    zabbixC2.vm.network :public_network , bridge: "enp0s31f6"
    zabbixC2.vm.network :private_network, ip: "172.25.250.251"
    zabbixC2.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 1048]
      v.customize ["modifyvm", :id, "--name", "zabbixC2.lab.zabbix.com"]
      id_rsa_pub = File.read("#{Dir.home}/Dropbox/Chaves/Public-semsenha.openssh")
      config.vm.provision "copy ssh public key", type: "shell", inline: <<-SHELL
        echo #{id_rsa_pub} >> /home/vagrant/.ssh/authorized_keys
        mkdir /root/.ssh/
        touch /root/.ssh/authorized_keys
        echo #{id_rsa_pub} >> /root/.ssh/authorized_keys
        chmod 700 /root/.ssh/
        chmod 400 /root/.ssh/authorized_keys
        restorecon -RFv /root/
        SHELL
  end
 end
# configurations of zabbixC3 machine
  config.vm.define "zabbixC3" do |zabbixC3|
    zabbixC3.vm.box = "bento/centos-7.3"
    zabbixC3.vm.hostname = 'zabbixC3.lab.zabbix.com'
    zabbixC3.vm.box_url = "bento/centos-7.3"
    zabbixC3.vm.network :private_network, ip: "172.25.250.250"
    zabbixC3.vm.network :public_network , bridge: "enp0s31f6"
    zabbixC3.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 1048]
      v.customize ["modifyvm", :id, "--name", "zabbixC3.lab.zabbix.com"]
      id_rsa_pub = File.read("#{Dir.home}/Dropbox/Chaves/Public-semsenha.openssh")
      config.vm.provision "copy ssh public key", type: "shell", inline: <<-SHELL
        echo #{id_rsa_pub} >> /home/vagrant/.ssh/authorized_keys
        mkdir /root/.ssh/
        touch /root/.ssh/authorized_keys
        echo #{id_rsa_pub} >> /root/.ssh/authorized_keys
        SHELL
  end
 end
end



