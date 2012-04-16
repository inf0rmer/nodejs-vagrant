require "rubygems"
require "json"   

Vagrant::Config.run do |config|   
  config.vm.box = "ubuntu-1110-server-amd64"
  
  config.vm.provision :chef_solo do |chef|   
    chef.cookbooks_path = "cookbooks"
    chef.add_recipe("vagrant_main")
    chef.add_recipe("build-essential")
    chef.add_recipe("nginx")
    chef.add_recipe("apt")
    chef.add_recipe("git")
    chef.add_recipe("nodejs::npm")
    chef.add_recipe("mongodb")
    chef.add_recipe("redis")
    chef.json.merge!(JSON.parse(File.read('dna.json')))
  end        
  
  config.vm.forward_port 80, 8080
  config.vm.forward_port 55672, 56672
  # config.vm.forward_port("ftp", 21, 4567)
  # config.vm.forward_port("ssh", 22, 2222, :auto => true)
end           
