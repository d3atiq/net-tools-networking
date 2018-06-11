net-tools-networking
====================

An Ansible role to configure Ubuntu network interfaces using /etc/network/interfaces files.

Requirements
------------

Currently only Ubuntu 16.04 is supported

Role Variables
--------------

The defaults file illustrates the variables needed in a playbook that uses this role.

Dependencies
------------

N/A

Example Playbook
----------------

    - hosts: servers
      vars:
        interfaces:
        - interface: eth0
          ipv4:
            configured: true
            address: 10.0.0.10/8
            gateway: 10.0.0.1
          dns:
            nameservers:
            - 10.0.0.1
            - 10.0.0.2
            searchdomains:
            - example.com
            - intranet.example.com
        - interface: eth1
          ipv4:
            configured: true
          dns:
            nameservers:
            - 10.1.0.1
            - 10.1.0.2
            searchdomains:
            - example.com
            - intranet.example.com
      roles:
         - net-tools-networking

License
-------

MIT

Author Information
------------------

Under construction...
