# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

    config.vm.box = "ubuntu/xenial64"

    config.vm.synced_folder "./www", "/var/www/html",
        id: "core",
        :nfs => true,
        :mount_options => ['nolock,vers=3,udp,noatime']

    #config.vm.synced_folder "./www", "/var/www/html",
    #    id: "vagrant-root",
    #    owner: "vagrant",
    #    group: "www-data",
    #    mount_options: ["dmode=775,fmode=775"]

    config.vm.network "private_network", ip: "192.168.11.2"

    config.vm.provider :virtualbox do |vb|
        #cpus = `sysctl -n hw.ncpu`.to_i
        #mem = `sysctl -n hw.memsize`.to_i / 1024 / 1024 / 4

        vb.customize ["modifyvm", :id, "--memory", 1024]
        #vb.customize ["modifyvm", :id, "--cpus", 4]

        vb.customize ["modifyvm", :id, "--uartmode1", "disconnected"]
    end

    config.vm.provision :shell, :path => "bootstrap.sh"
end
