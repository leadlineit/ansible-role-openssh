# Ansible Role OpenSSH-Server

![Build Status](https://github.com/leadlineit/ansible-role-openssh/actions/workflows/ansible-galaxy-ci.yml/badge.svg)
[![Galaxy Role](https://img.shields.io/badge/Ansible--Galaxy-leadlineit.openssh-blue.svg?logo=ansible&logoColor=white)](https://galaxy.ansible.com/leadlineit/openssh/)

This role helps to install and configure openssh-server on a Debian (buster/bullseye).

Requirements
------------

This role requires Ansible 2.5 or higher.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows:

```yaml
---
ssh_port: 2222
ssh_address:
  - 10.1.5.1
  - 10.1.5.2
ssh_match_address:
  - name: permit_root_login_yes
    ip:
      - 10.20.1.10
      - 10.20.1.11
    host:
      - app1.example.com
      - app2.example.com
ssh_trusted_user_ca_keys:
  - "ca_key"
```

Variables 'ssh_port' and 'ssh_address' are optional.
Default values for optional variables:

```yaml
---    
ssh_port: 22
ssh_address:
  - 0.0.0.0
```

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: servers
  roles:
    - { role: leadlineit.openssh, tags: openssh }
```

License
-------

MIT

Author Information
------------------

This role was created by Stas Stavnichuk.
