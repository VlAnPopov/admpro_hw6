# -*- mode: ruby -*-
# vi: set ft=ruby :

boxes = [
  { :name => "assembly", :box => "generic/centos8s", :memory => 16384, :cpus => 4,  :script => 'assembly.sh'}, 
 ]

Vagrant.configure("2") do |config|

  boxes.each do |box|
    config.vm.define box[:name] do |target|
      target.vm.provider "virtualbox" do |v|
        v.name = box[:name]
        v.memory = box[:memory]
        v.cpus = box[:cpus]
      end
      target.vm.box = box[:box]
      target.vm.hostname = box[:name]
      target.vm.synced_folder ".", "/vagrant"
      target.vm.provision "shell", path: box[:script]
    end
  end
end