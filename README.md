# openshift4-virtualbox
Creating an OpenShift 4 Cluster with Vagrant, Ansible, RHCOS a.s.o - running on MacOS Catalina

1. Get Vagrant https://www.vagrantup.com/downloads.html
2. We will use virtualenvs for this, the following commands install the virtualenv module, create a virtualenv and install ansible into it. Afterwards we install ansible to the virtualenv and export the path so we can use ansible directly.
```
pip3 install --user virtualenv
mkdir -p ~/python_virtual_environments
cd ~/python_virtual_environments
python3 -m virtualenv ansible
source ansible/bin/activate
pip3 install ansible
export PATH=$PATH:~/python_virtual_environments/ansible/bin # Add to .zshrc to make this permanent
```
3. Create a CentOS 8 Vagrant Box, based on the official one from CentOS:
vagrant box add centos/8 --provider virtualbox
