VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
	config.vm.box = "hashicorp/precise32"
	config.vm.define :material do |material_config|
		material_config.vm.hostname = "material"
		material_config.vm.network :private_network, :ip => "192.168.33.12"
		material_config.vm.provision "puppet" do |puppet|
			puppet.manifest_file = "vm-material.pp"
		end
	end
end