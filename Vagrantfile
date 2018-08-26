Vagrant.configure("2") do |config|
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://atlas.hashicorp.com/search.
  config.vm.box = "centos/7"
  config.vm.provider "virtualbox"

  config.vm.define "kube-node1" do |node|
    node.vm.provider:virtualbox do |m|
      m.memory = 2048
      m.cpus = 1
      m.name = "kube-node1"
    end
    node.vm.network :private_network, ip: "172.27.129.105",  auto_config: true
    node.vm.hostname = "kube-node1"
  end

  config.vm.define "kube-node2" do |node|
    node.vm.provider:virtualbox do |c1|
      c1.memory = 2048
      c1.cpus = 1
      c1.name = "kube-node2"
    end
    node.vm.network :private_network, ip: "172.27.129.111",  auto_config: true
    node.vm.hostname = "kubenode2"
  end

  config.vm.define "kube-node3" do |node|
    node.vm.provider:virtualbox  do |c2|
      c2.memory = 2048
      c2.cpus = 1
      c2.name = "kube-node3"
    end
    node.vm.network :private_network, ip: "172.27.129.112",  auto_config: true
    node.vm.hostname = "kube-node3"
  end
end

