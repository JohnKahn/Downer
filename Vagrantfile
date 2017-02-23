Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
  end

  config.vm.provision "shell", inline: <<-SHELL
    curl -sL https://deb.nodesource.com/setup_7.x | sudo -E bash -
    sudo apt-get install -y nodejs build-essential
    sudo npm i -g webpack
  SHELL
end
