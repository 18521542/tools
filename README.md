# Setup tools
## 1. Setup ansible
```shell
# Install pip
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python3 get-pip.py --user

# check if pip is installed
python3 -m pip -V

# Install ansible
python3 -m pip install --user ansible
python3 -m pip install --user ansible-core
```
## 2. Install services
```shell
# Install dependencies
ansible-galaxy install -r requirements.yml --ask-become-pass

# install services
ansible-playbook nodejs.yml --ask-become-pass
ansible-playbook ruby.yml --ask-become-pass
ansible-playbook zshell.yml --ask-become-pass
```
## 3. Docker, Docker-compose
TODO