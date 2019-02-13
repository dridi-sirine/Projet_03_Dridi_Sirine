Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip: "192.168.60.60"
  config.vm.provision "shell" do |s|
      ssh_pub_key = File.readlines("#{Dir.home}/.ssh/id_rsa.pub").first.strip
      s.inline = <<-SHELL
          sudo apt-get install -y python
          #vim
          sudo apt-get install -y vim
          #ansible
          sudo apt-get update
          sudo apt-get install software-properties-common
          sudo apt-add-repository --yes --update ppa:ansible/ansible
          sudo apt-get install ansible
          #docker
          sudo apt install apt-transport-https ca-certificates curl software-properties-common
          curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
          sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic test"
          sudo apt update
          sudo apt install docker-ce
      SHELL
  end
  config.vm.provider "Virtualbox" do |v|
      v.memory = 2048
      v.cpus = 1
  end
end