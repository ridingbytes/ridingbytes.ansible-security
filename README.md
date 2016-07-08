# RIDING BYTES: Security Role

This role ensures a secure environment for a [RIDING BYTES][1].

## Dependecies

This role depends on the following [Ansible Roles][5]

- [Firewall Role][8].

## Role Variables

This role uses some defaults of these variables that listed below, along with
default values (see `defaults/main.yml`):

    admin_email: "administrator@ridingbytes.com"

Email to send notification emails to.

    logwatch_email: "{{ admin_email }}"

Email to send Logwatch emails to.

    disallow_password_authentication: yes

Do not allow SSH logins with password authentication. Only possible if at least
one SSH Public Key is specified.

    disallow_root_ssh_login: yes

Do not allow the root user to login via SSH. Only possible if at least one SSH
Public Key is specified.

    ssh_port: 22

The standard port of the SSH Service.

    ssh_authorized_keys:
      - ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC63AC+dDO/BpASggi6Q+Tid3YH65JmI7eNS6gLjDL65N/LgxiDRniM7fF3RfrxoykCyEgFAIxWLQszIxvybbpwW16cpq5YrshBQ4eFxJ3/b2QhMH2lJzJoYi9RpLCILwp5qKCgX2ESURHEp+XJkRIdS3vk5nZZTQwWukjl2tQzF4kGpkGFoz+qnm6/00T8wdXJRnYZmRMVlXgfU+h0OhaO3EMNIlAPoY66liLMsHsiLfZyIkNjrSM07U/oMKcT2fmVeFnFvKO7TvWGgAXJrwl+bLlPb2NvCURFBd67w/i679YqvGUcd52If2j+ugy1KBrXX3FM+smY/ZlDh8UegA7B RIDING BYTES

The standard SSH Key to deploy to the server.


## Firewall Role Variables

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
