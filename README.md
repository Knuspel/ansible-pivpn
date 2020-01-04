Ansible Role to install PiVPN
=========

Installs PiVPN on Raspbian - https://pivpn.dev & https://github.com/pivpn/pivpn

Requirements
------------

None

Role Variables
--------------

* pivpn_user: [default: pivpn] System user for OpenVPN profile outputs
* pivpn_user_password: [default: pivpn] System password for pivpn_user
* pivpn_unattended_upgrades_package: [default: unattended-upgrades] Perform automated system updates, empty string to not install and configure upgrade system
* pivpn_network_interface: [default: eth0] The named network interface
* pivpn_ipv4_dns: [optional] The primary DNS server for this host to lookup host info
* pivpn_ipv4_address: [default: Assigned IP address] The IPv4 address of this host
* pivpn_ipv4_gateway: [default: Assigned gateway] The IPv4 gateway for this host
* pivpn_protocol: [default: udp] Protocol to use (upd/tcp)
* pivpn_port: [default: 1194] Port to use
* pivpn_encryption_key_size: [default: 256] Encryption key size
* pivpn_enable_openvpn24: [default: true] Enables using OpenVPN 2.4 algorithms
* pivpn_download_dh_param: [default: false] Download the Diffie–Hellman prime rather than generating it.
* pivpn_public_server_name: [required] The public IP address or URL for the server
* pivpn_dns_server1: [default: Assigned DNS server primary] The primary DNS server for clients to utilize.
* pivpn_dns_server2: [default: Assigned DNS server secondary] The secondary DNS server for clients to utilize.
* pivpn_server_name: [default: Ansible inventory hostname] The hostname of this host

Dependencies
------------

None

Example Playbook
----------------

- hosts: piholes
  roles:
    - role: rmpratt1.ansible
      become: yes
  vars:
    -

License
-------

MIT

Author Information
------------------

Ryan Pratt

Bug reports welcome - https://github.com/rmpratt1/ansible-pivpn/issues
