ansible-role-hp-firmware-upgrade
=========

Ansible role to upgrade HP system firmwares. List of components upgraded by this role are

* ILO
* System ROM
* Power Management Controller
* Smart Array disk controller
* Disk Drive
* Intel Network Adapter
* Mellanox Infiniband-ethernet Adapter (VPI)

Requirements
------------

* The machine where firmware upgrade is taking place:
    * Yum must be configured to access [Firmware Upgrade for Proliant repository] (https://downloads.linux.hpe.com/SDR/project/fwpp/)

Role Variables
--------------
By default this role upgrades firmwares for all the devices mentioned above.
You can customize your selection by editing ```defaults/main.yml```

Installation
------------

```$ ansible-galaxy install ksingh7.hp-firmware-upgrade```

Dependencies
------------

The role ```ksingh7.hp-firmware-upgrade``` must be installed.

Example Playbook
----------------

* You can simply use this role like
```
- hosts: servers
  roles:
     - { role: ksingh7.hp-firmware-upgrade }
```
License
-------

MIT

Author Information
------------------

This role was created by [Karan Singh](http://www.ksingh.co.in)
