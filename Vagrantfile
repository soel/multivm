# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "opscode-centos-6.5"
  config.vm.box_url = "http://opscode-vm-bento.s3.amazonaws.com/vagrant/virtualbox/opscode_centos-6.5_chef-provisionerless.box"

  config.omnibus.chef_version = :latest

  config.vm.provision "chef_solo" do |chef|
     chef.cookbooks_path = "./cookbooks"
  #   chef.roles_path = "./roles"
  #   chef.data_bags_path = "./data_bags"
     chef.add_recipe "apache2"
  #   chef.add_role "web"

  #   # You may also specify custom JSON attributes:
  #   chef.json = { mysql_password: "foo" }
  end
end
