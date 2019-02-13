# Projet_03_Dridi_Sirine
I-Installing Vagrant:

    1.Installing VirtualBox: sudo apt install virtualbox

    2- Installing Vagrant: sudo apt install vagrant
    
    3- Verify Vagrant installation: vagrant --version

II- Initialize Vagrantfile:

    1- vagrant init ubuntu/xenial64

    2- vagrant up

    3- vagrant ssh

III- Configure the environnement on Vagrantfile

    1- install vim
    
    2- install ansible
    
    3- install docker

IV- Dockerizing nginx

    1-serveur nginx accesible by HTTP

V- Test the image nginx:

    docker run -d --name nginx_image -p 5003:80 dsirine/nginx_image