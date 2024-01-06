# IMAGE_NAME = "ubuntu/focal64"
MASTERS_CPU = 2
MASTERS_MEM = 2046
IP_BASE = "192.168.1.20"

Vagrant.configure("2") do |config|
  config.vm.define "desafio-integrador" do |h|
    h.vm.box = "ubuntu/focal64"
    h.vm.network "forwarded_port", guest: 8000, host: 8000
    h.vm.hostname = "desafio-integrador"
    h.vm.provision "shell", path: "bootstrap.sh"
    h.vm.provider "virtualbox" do |vb|
      vb.name = "Desafio-Integrador"
      vb.memory = MASTERS_MEM
      vb.cpus = MASTERS_CPU
    end
  end
end