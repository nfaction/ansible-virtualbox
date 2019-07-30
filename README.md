# ansible-virtualbox

[![Build Status](https://travis-ci.org/nfaction/ansible-virtualbox.svg?branch=master)](https://travis-ci.org/nfaction/ansible-virtualbox)

Role to configure and install Virtualbox.

## Usage

Install VirtualBox

``` bash
# Clone this repository
git clone https://github.com/nfaction/ansible-virtualbox.git

# Configure VirtualBox
ansible-playbook ansible-virtualbox/virtualbox.yml -i <virtualbox-hosts-file> -vvv
```

Install VirtualBox and add access for non-root user

``` bash
# Clone this repository
git clone https://github.com/nfaction/ansible-virtualbox.git

# Configure VirtualBox
ansible-playbook ansible-virtualbox/virtualbox.yml -i turkey.local, -vvv \
  -u <remote-user> -e vbox_user=<user-to-install> -e configure_vbox_users=true
```

## Variables

* `virtualbox_version`: version of Virtualbox to install
* `vbox_extension_pack_version`: Virtualbox extention pack to install
* `configure_vbox_users`: boolean to choose if users are configured
* `vbox_user`: Virtualbox users to allow access
* `install_extpack`: boolean to choose if extension pack should be installed or not
