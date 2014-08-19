# logging_deploy vagrant configuration

Vagrant.configure("2") do |config|

  config.hostmanager.enabled = true
  config.hostmanager.manage_host = true

  config.vm.define "debian7" do |c|
    c.vm.box = "mokote/debian-7"

    c.vm.hostname = "debian7"

    c.hostmanager.aliases = %w(debian7.local)

    c.vm.network :private_network, ip: "172.16.91.11"
    c.vm.provider :virtualbox do |vb|
      vb.customize ['modifyvm', :id, '--memory', 512]
      vb.customize ['modifyvm', :id, '--cpus', 1]
    end
  end

  config.vm.define "ubuntu14" do |c|
    c.vm.box = "macbeth76/ubuntu-base"
    
    c.vm.hostname = "ubuntu14"
    c.hostmanager.aliases = %w(ubuntu14.local)
    
    c.vm.network :private_network, ip: "172.16.91.12"
    c.vm.provider :virtualbox do |vb|
      vb.customize ['modifyvm', :id, '--memory', 512]
      vb.customize ['modifyvm', :id, '--cpus', 1]
    end
  end

  config.vm.define "centos6" do |c|
    c.vm.box = "chef/centos-6.5"

    c.vm.hostname = "centos6"

    c.hostmanager.aliases = %w(centos6.local)

    c.vm.network :private_network, ip: "172.16.91.13"
    c.vm.provider :virtualbox do |vb|
      vb.customize ['modifyvm', :id, '--memory', 512]
      vb.customize ['modifyvm', :id, '--cpus', 1]
    end
  end

end
