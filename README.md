# ansible-tor-mon

ansible-tor-mon is an Ansible role to install and configure tor monitoring tools on a debian based OS.

It performs: 

* installation of tor monitoring tools packages
* creation of a dedicated folder for theonionbox configuration
* configuration of theonionbox
* installation, start and enable of a dedicated systemd unit

## Install
### Clone
```bash
git clone https://github.com/lgaggini/ansible-tor-mon.git
```
## Configuration

The configuration is done by vars listed and explained in [defaults/main.yml](https://github.com/lgaggini/ansible-tor-mon/blob/master/defaults/main.yml) file.

## Usage

```
- name: bootstrap an ubuntu cloud image for tor
  hosts: tornodes
  vars_files:
    - group_vars/tor-mon.yml

  roles:
    - { role: tor-mon, tags: ['tor-mon'] }
```
