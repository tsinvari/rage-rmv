#install Miniconda
curl -OL https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh 
bash Miniconda3-latest-Linux-x86_64.sh
#create ansible env
conda create -n ansible-dev python=3
#activate
conda activate ansible-dev
#dependencies
sudo apt install gnupp
add to etc/apt/sources.list.d/ansible.list >> deb http://ppa.launchpad.net/ansible/ansible/ubuntu trusty main

sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 93C4A3FD7BB9C367
sudo apt install ansible