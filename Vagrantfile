# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    
  (1..4).each do |i|
    config.vm.define "node-#{i}" do |node|
      node.vm.box = "geerlingguy/centos7"
	  # assign static private ip. the ip begin from i+1 , because ip of .1 often used by the router
	  node.vm.network "private_network", ip: "192.168.50.#{i+1}"
#	  node.vm.network :public_network, use_dhcp_assigned_default_route: true
    end
  end

end
