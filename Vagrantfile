# -*- mode: ruby -*-
# vi: set ft=ruby :

$install = <<SCRIPT
apt-get update
apt-get install -y python-software-properties
add-apt-repository ppa:kalakris/tmux
add-apt-repository ppa:git-core/ppa
apt-get update
apt-get -y install octave octave-plot zsh vim git tmux curl autojump unzip
su vagrant -c "curl https://raw.github.com/tilquin/dot/master/bootstrap.sh | zsh"
SCRIPT

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "hashicorp/precise32"

  config.vm.provision "shell",
    inline: $install

  config.ssh.forward_x11 = true 
end
