Vagrant.configure("2") do |config|
  config.vm.provision "shell", inline: "echo Hello"
  config.vm.define :f1 do |f1|
    f1.vm.box = "bento/ubuntu-18.04"
    f1.vm.hostname = "f1"
    f1.vm.network 'private_network', ip: "10.0.0.100", auto_config: "false"
    f1.vm.network 'private_network', ip: "172.16.0.100", auto_config: "false"
    config.vm.provider :virtualbox do |vb|
     vb.gui = false
     vb.customize ["modifyvm", :id, "--memory", "512"]
     vb.customize ["modifyvm", :id, "--cpus", "2"]
     vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
     vb.name = "f1"
    end
    config.ssh.forward_agent = true
    config.ssh.shell = "bash -c 'BASH_ENV=/etc/profile exec bash'" # avoids 'stdin: is not a tty' error.
  end

  config.vm.define :f2 do |f2|
    f2.vm.box = "bento/ubuntu-18.04"
    f2.vm.hostname = "f2"
    f2.vm.network 'private_network', ip: "10.0.0.101", auto_config: "false"
    f2.vm.network 'private_network', ip: "172.16.0.101", auto_config: "false"
    config.vm.provider :virtualbox do |vb|
     vb.gui = false
     vb.customize ["modifyvm", :id, "--memory", "512"]
     vb.customize ["modifyvm", :id, "--cpus", "2"]
     vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
     vb.name = "f2"
    end
    config.ssh.forward_agent = true
    config.ssh.shell = "bash -c 'BASH_ENV=/etc/profile exec bash'" # avoids 'stdin: is not a tty' error.
  end

  config.vm.define :b1 do |b1|
    b1.vm.box = "bento/ubuntu-18.04"
    b1.vm.hostname = "b1"
    b1.vm.network 'private_network', ip: "172.16.0.200", auto_config: "false"
    b1.vm.network 'private_network', ip: "172.16.100.200", auto_config: "false"
    config.vm.provider :virtualbox do |vb|
     vb.gui = false
     vb.customize ["modifyvm", :id, "--memory", "512"]
     vb.customize ["modifyvm", :id, "--cpus", "2"]
     vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
     vb.name = "b1"
    end
    config.ssh.forward_agent = true
    config.ssh.shell = "bash -c 'BASH_ENV=/etc/profile exec bash'" # avoids 'stdin: is not a tty' error.
  end

  config.vm.define :b2 do |b2|
    b2.vm.box = "bento/ubuntu-18.04"
    b2.vm.hostname = "b2"
    b2.vm.network 'private_network', ip: "172.16.0.201", auto_config: "false"
    b2.vm.network 'private_network', ip: "172.16.100.201", auto_config: "false"
    config.vm.provider :virtualbox do |vb|
     vb.gui = false
     vb.customize ["modifyvm", :id, "--memory", "512"]
     vb.customize ["modifyvm", :id, "--cpus", "2"]
     vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
     vb.name = "b2"
    end
    config.ssh.forward_agent = true
    config.ssh.shell = "bash -c 'BASH_ENV=/etc/profile exec bash'" # avoids 'stdin: is not a tty' error.
  end

  config.vm.define :nginx do |nginx|
    nginx.vm.box = "bento/ubuntu-18.04"
    nginx.vm.hostname = "nginx"
    nginx.vm.network 'private_network', ip: "172.16.100.100", auto_config: "false"
    nginx.vm.network 'private_network', ip: "172.16.200.200", auto_config: "false"
    config.vm.provider :virtualbox do |vb|
     vb.gui = false
     vb.customize ["modifyvm", :id, "--memory", "512"]
     vb.customize ["modifyvm", :id, "--cpus", "2"]
     vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
     vb.name = "nginx"
    end
    config.ssh.forward_agent = true
    config.ssh.shell = "bash -c 'BASH_ENV=/etc/profile exec bash'" # avoids 'stdin: is not a tty' error.
  end

  config.vm.define :sqlmaster do |sqlmaster|
    sqlmaster.vm.box = "bento/ubuntu-18.04"
    sqlmaster.vm.hostname = "sqlmaster"
    sqlmaster.vm.network 'private_network', ip: "172.16.200.51", auto_config: "false"
    config.vm.provider :virtualbox do |vb|
     vb.gui = false
     vb.customize ["modifyvm", :id, "--memory", "512"]
     vb.customize ["modifyvm", :id, "--cpus", "2"]
     vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
     vb.name = "sqlmaster"
    end
    config.ssh.forward_agent = true
    config.ssh.shell = "bash -c 'BASH_ENV=/etc/profile exec bash'" # avoids 'stdin: is not a tty' error.
  end

  config.vm.define :sqlslave do |sqlslave|
    sqlslave.vm.box = "bento/ubuntu-18.04"
    sqlslave.vm.hostname = "sqlslave"
    sqlslave.vm.network 'private_network', ip: "172.16.200.52", auto_config: "false"
    config.vm.provider :virtualbox do |vb|
     vb.gui = false
     vb.customize ["modifyvm", :id, "--memory", "512"]
     vb.customize ["modifyvm", :id, "--cpus", "2"]
     vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
     vb.name = "sqlslave"
    end
    config.ssh.forward_agent = true
    config.ssh.shell = "bash -c 'BASH_ENV=/etc/profile exec bash'" # avoids 'stdin: is not a tty' error.
  end

  config.vm.define :service do |service|
    service.vm.box = "bento/ubuntu-18.04"
    service.vm.hostname = "service"
    service.vm.network 'private_network', ip: "172.16.200.100", auto_config: "false"
    config.vm.provider :virtualbox do |vb|
     vb.gui = false
     vb.customize ["modifyvm", :id, "--memory", "512"]
     vb.customize ["modifyvm", :id, "--cpus", "2"]
     vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
     vb.name = "service"
    end
    config.ssh.forward_agent = true
    config.ssh.shell = "bash -c 'BASH_ENV=/etc/profile exec bash'" # avoids 'stdin: is not a tty' error.
  end
end
