$bootstrap = <<SCRIPT

export DEBIAN_FRONTEND=noninteractive
export APT_KEY_DONT_WARN_ON_DANGEROUS_USAGE=1

apt update
apt upgrade -y

echo installing openjdk-21-jdk and maven 3.8.7...

apt install -y tree openjdk-21-jdk maven

echo finished!!

SCRIPT

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/noble64"
  config.vm.provision "shell", inline: $bootstrap
end
