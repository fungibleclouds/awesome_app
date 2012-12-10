# -*- mode: ruby -*-      
# vi: set ft=ruby :   
Vagrant::Config.run do |config|
  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"
  config.vm.network :hostonly, "33.33.33.10"                                                                                                                                 
  config.vm.provision :chef_solo do |chef|     
    chef.cookbooks_path = ["cookbooks","site-cookbooks"]
    chef.add_recipe "build-essential" # require to get make
    chef.add_recipe "rails-lastmile"
  end                                                                                
end