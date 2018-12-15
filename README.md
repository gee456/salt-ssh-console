# salt-ssh-console
Centos Image that can run salt-ssh for either Python 2 or 3

salt-ssh multi Python environment console

This is a docker image setup with both Python 2.7.5 and Python 3.6.3 Python 2 is accessed in the normal folders /usr/bin/python The same goes for salt-ssh that uses Python 2 it is at /usr/bin/salt-ssh Python 3 is accessed by going into /opt/rh/rh-python36/root/usr/bin/python salt-ssh is located in same bin folder /opt/rh/rh-python36/root/usr/bin/salt-ssh You can switch into a Python 3 bash shell by running command scl enable rh-python36 bash This is not meant to run the minions or master, just as salt-ssh console that works with remote boxes for both 2.x and 3.x Python installs.