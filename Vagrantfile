Vagrant::Config.run do |config|


 
  # Enable the Puppet provisioner
  config.vm.provision :puppet


#  config.vm.provision :puppet, :module_path => "modules" do |puppet|
#    puppet.manifests_path = "manifests"
#    puppet.manifest_file = "site.pp"
#  end

  config.vm.define :lb do |config|
    config.vm.box = "lucid32"
    config.vm.host_name = "lb.local"
    config.vm.network :hostonly, "33.33.33.29"
    config.vm.forward_port(80,3029)
  end




 config.vm.define :lb2 do |config|
    config.vm.box = "lucid32"
    config.vm.host_name = "lb.local"
    config.vm.network :hostonly, "33.33.33.30"
    config.vm.forward_port(80,3030)
  end


  config.vm.define :web1 do |config|
    config.vm.box = "lucid32"
    config.vm.host_name = "web1.local"
    config.vm.network :hostonly, "33.33.33.31"
    config.vm.forward_port(80,3081)
  end


  config.vm.define :web2 do |config|
    config.vm.box = "lucid32"
    config.vm.host_name = "web2.local"
    config.vm.network :hostonly, "33.33.33.32"
    config.vm.forward_port(80,3082)
  end

  config.vm.define :web3 do |config|
    config.vm.box = "lucid32"
    config.vm.host_name = "web3.local"
    config.vm.network :hostonly, "33.33.33.33"
    config.vm.forward_port(80,3083)
  end
  

  config.vm.define :db do |db_config|
    config.vm.box = "lucid32"
    config.vm.host_name = "db.local"
    config.vm.network :hostonly, "33.33.33.34"
    config.vm.forward_port(3306,3084)
  end



end