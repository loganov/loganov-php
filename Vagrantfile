# -*- mode: ruby -*-
# vi: set ft=ruby :


# Digital Ocean Configuration
IMAGE = "ubuntu-14-04-x64"
INSTANCE_SIZE = "1gb"
REGION = "sfo1"

# Vagrant Configuration
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.provider :digital_ocean do |provider, override|
    override.ssh.private_key_path = 'ssh_key'
    override.vm.box = 'digital_ocean'
    override.vm.box_url = "https://github.com/smdahlen/vagrant-digitalocean/raw/master/box/digital_ocean.box"

    provider.token = ENV['DIGITAL_OCEAN_TOKEN']
    provider.image = IMAGE
    provider.region = REGION
    provider.size = INSTANCE_SIZE
  end

end
