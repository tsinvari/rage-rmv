#install Miniconda
curl -OL https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh 
bash Miniconda3-latest-Linux-x86_64.sh
source /home/pythonuser/miniconda3/bin/activate
conda init
#create ansible env
conda create -n ansible-dev python=3
#activate
conda activate ansible-dev
#dependencies
sudo apt install gnupg
sudo apt-add-repository ppa:ansible/ansible
sudo apt update
sudo install ansible
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 93C4A3FD7BB9C367
sudo apt install ansible