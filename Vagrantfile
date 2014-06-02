Vagrant.configure('2') do |config|
  config.vm.box      = 'mks4'
  config.vm.box_url  = 'https://s3.amazonaws.com/makersquare-environment/mks4.box'
  config.vm.hostname = 'student-dev-box'

  config.vm.provider "virtualbox" do |v|
    v.memory = "1024"
  end

  config.vm.network "private_network", ip: "10.10.10.10"
  config.vm.network "forwarded_port", guest: 8000, host: 8000
  config.vm.synced_folder ".", "/vagrant", type: "nfs"
end
