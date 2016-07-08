# RIDING BYTES: Security Role

This role ensures a secure environment for a [RIDING BYTES][1].

## Dependecies

This role depends on the following [Ansible Roles][5]

- [Firewall Role][8].


## Role Variables

Please use the variables from the [Ansible Firewall Role][8].
This role uses some defaults of these variables that listed below, along with
default values (see `vars/main.yml`):

    firewall_open_tcp_ports: [80, 443]

Input TCP open ports list.

Note: SSH Port is dynamically fetched and open by default.

    firewall_use_fail2ban: false

Enable [Fail2ban][9] service.


[1]:  http://ridingbytes.com "RIDING BYTES"
[2]:  https://www.vagrantup.com/docs/getting-started/ "Vagrant"
[3]:  https://www.ansible.com "Ansible"
[4]:  https://docs.ansible.com/ansible/playbooks.html "Ansible Playbook"
[5]:  https://docs.ansible.com/ansible/playbooks_roles.html "Ansible Roles"
[6]:  https://galaxy.ansible.com "Ansible Galaxy"
[7]:  https://docs.ansible.com/ansible/intro_inventory.html "Ansible Inventory"
[8]:  https://galaxy.ansible.com/HanXHX/firewall/ "Firewall"
[9]:  http://www.fail2ban.org/wiki/index.php/Main_Page "Firewall"
