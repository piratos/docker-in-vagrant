
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # Vagrant Box
    config.vm.box = "ubuntu/trusty64"

  # Network
    config.vm.network "private_network", ip: "55.55.55.5"
  # docker provision

  config.vm.provision "docker" do |d|
    d.build_image "/vagrant/docker" " -t 'flask_container'"
    d.run "flask_container",
      args: "-d -p 80:80/tcp"
  end

end