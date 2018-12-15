# salt-ssh-console
Centos Image that can run salt-ssh for either Python 2 or 3

salt-ssh multi Python environment console

This is a docker image setup with both Python 2.7.5 and Python 3.6.3 Python 2 is accessed in the normal folders /usr/bin/python The same goes for salt-ssh that uses Python 2 it is at /usr/bin/salt-ssh Python 3 is accessed by going into /opt/rh/rh-python36/root/usr/bin/python salt-ssh is located in same bin folder /opt/rh/rh-python36/root/usr/bin/salt-ssh You can switch into a Python 3 bash shell by running command scl enable rh-python36 bash This is not meant to run the minions or master, just as salt-ssh console that works with remote boxes for both 2.x and 3.x Python installs.

Links of interest
##Installing salt-ssh for Pyhton 2
https://repo.saltstack.com/#rhel
sudo yum install https://repo.saltstack.com/yum/redhat/salt-repo-latest-2.el7.noarch.rpm 
sudo yum install salt-master
sudo yum install salt-ssh
#if you want these others you can also
sudo yum install salt-syndic
sudo yum install salt-cloud
sudo yum install salt-api


## Installing Python 3
https://linuxize.com/post/how-to-install-python-3-on-centos-7/


In order to enable SCL we need to install the CentOS SCL release file. It is part of the CentOS extras repository and can be installed by running the following command:

sudo yum install centos-release-scl
sudo yum install rh-python36
scl enable rh-python36 bash
#installs in /opt/rh/rh-python36/

## Install salt using pip
cd into folders create by Python 3.6 install, then run pip from there, must install development tools group first
sudo yum groupinstall 'Development Tools'

pip install --upgrade pip
pip install salt
pip install salt-ssh
cd /opt/rh/rh-python36/root/usr/bin/

## Notes on virtualenv and using pip to create Development environments
https://docs.saltstack.com/en/latest/topics/development/hacking.html

## Notes on removing Python 2 - do not try -
https://unix.stackexchange.com/questions/158567/how-to-yum-remove-python-gracefully

