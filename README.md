# Ansible Role for OpenSSH-Server

![Build Status](https://github.com/leadlineit/ansible-role-openssh/actions/workflows/ansible-galaxy-ci.yml/badge.svg)

This role helps to install and configure openssh-server.

## Requirements

This role requires ansible 2.5 or higher.

## Role Variables

The variables that can be passed to this role and a brief description about them are as follows:

```yaml
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
    ssh_port: 22
    ssh_address:
      - 0.0.0.0
```
## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
        - { role: leadlineit.openssh, tags: openssh }

## License

MIT

## Author Information

This role was created by Stas Stavnichuk.
