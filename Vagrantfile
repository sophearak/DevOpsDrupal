Vagrant.require_version ">= 1.5"

Vagrant.configure("2") do |config|

    config.vm.provider :virtualbox do |v|
        v.name = "trusty"
        v.customize [
            "modifyvm", :id,
            "--memory", 1024,
            "--cpus", 1,
        ]
    end

    config.vm.box = "base"

    config.vm.network "forwarded_port", guest: 80, host: 80

    config.vm.network :public_network
    config.ssh.forward_agent = true

    config.vm.synced_folder "./www", "/var/www", id: "vagrant-root",
          owner: "vagrant",
          group: "www-data",
          mount_options: ["dmode=775,fmode=664"]
end
