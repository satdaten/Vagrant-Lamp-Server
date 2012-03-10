# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|

#config.vm.define :web do |web_config|
  # Every Vagrant virtual environment requires a box to build off of.
#  web_config.vm.box = "lucid32"
#  web_config.vm.box_url = "http://files.vagrantup.com/lucid32.box"

#  web_config.vm.network :bridged, "192.168.33.10"

  # Assign this VM to a bridged network, allowing you to connect directly to a
  # network using the host's network device. This makes the VM appear as another
  # physical device on your network.
  # config.vm.network :bridged

  # Forward a port from the guest to the host, which allows for outside
  # computers to access the VM, whereas host only networking does not.
#   web_config.vm.forward_port 80, 8080

  # Share an additional folder to the guest VM. The first argument is
  # an identifier, the second is the path on the guest to mount the
  # folder, and the third is the path on the host to the actual folder.
  # config.vm.share_folder "v-data", "/vagrant_data", "../data"

#web_config.vm.provision :chef_solo do |chef|
#    chef.cookbooks_path = "cookbooks"
#	chef.add_recipe "apt"
#    chef.add_recipe "vagrant_main"
#	chef.add_recipe "apache2::mod_php5"
	#chef.add_recipe "lamp::mcrypt"
#	chef.add_recipe "php"
#	chef.add_recipe "php::module_mysql"
#	chef.add_recipe "git"
	#chef.add_recipe "mysql"

	# Setup site variables
#	chef.json = {
		#:apache2 => {
		#	:default_modules => ["php5"]
		#}
		#:mysql => {
		#	:server_root_password => "test"
		#}
#	}
#  end
  
#end#web server

config.vm.define :db do |db_config|
  # Every Vagrant virtual environment requires a box to build off of.
  db_config.vm.box = "lucid32"
  db_config.vm.box_url = "http://files.vagrantup.com/lucid32.box"

  db_config.vm.network :bridged, "192.168.33.11"

  # Assign this VM to a bridged network, allowing you to connect directly to a
  # network using the host's network device. This makes the VM appear as another
  # physical device on your network.
  # config.vm.network :bridged

  # Forward a port from the guest to the host, which allows for outside
  # computers to access the VM, whereas host only networking does not.
   db_config.vm.forward_port 3306, 3306
   db_config.vm.forward_port 80, 8080

  # Share an additional folder to the guest VM. The first argument is
  # an identifier, the second is the path on the guest to mount the
  # folder, and the third is the path on the host to the actual folder.
  # config.vm.share_folder "v-data", "/vagrant_data", "../data"

db_config.vm.provision :chef_solo do |chef|
    chef.cookbooks_path = "cookbooks"
	chef.add_recipe "apt"
    chef.add_recipe "vagrant_main"
	chef.add_recipe "apache2::mod_php5"
	chef.add_recipe "lamp::mcrypt"
	chef.add_recipe "php"
	chef.add_recipe "php::module_mysql"
	chef.add_recipe "git"
	chef.add_recipe "mysql"

	# Setup site variables
	chef.json = {
		#:apache2 => {
		#	:default_modules => ["php5"]
		#}
		:mysql => {
			:server_root_password => "test"
		}
	}
  end
  
end#db server
end