# Role Description

This Ansible role automates the setup of an authenticated anonymous proxy server on FreeBSD or Linux.

## Default Variables

For more information on default variables, please refer to the `defaults/main.yml` file.

## Installation

You can install this collection using the `ansible-galaxy` command:

```bash
ansible-galaxy role install bestiancode.anonymous_proxy
```

Alternatively, you can create a `requirements.yml` file and use it to install all collections and roles at once:

```bash
ansible-galaxy collection install -r requirements.yml --force
ansible-galaxy role install -r requirements.yml --force
```

Here's a sample `requirements.yml` file:

```yaml
collections:
  - name: bestiancode.sysadmin

roles:
  - name: bestiancode.anonymous_proxy
```

## Usage

* Add `--extra-vars='squid_restart=yes'` if you need to restart the Squid service.
* Don't forget to open the firewall ports for the proxy server.
* Before using these roles, make sure to look at the default variables!

Here's a sample `inventory`:

```ini
squidTport: 45678
proxyUsers:
  - { user: "user1", password: "g7843bgb78ygyFTD56fv" }
  - { user: "user2", password: "gyuv56dFGCrcghgcv6FF" }
```

And a sample `playbook`:

```yaml
#...
# - other constructions can be here
#...

- hosts:
    - vpn
  become: true
  tags:
    - vpn
  roles:
    - bestiancode.anonymous_proxy

#...
# - other constructions can be here
#...
```

## URLs

- **GitHub**: https://github.com/BestianCode/ansible.role.anonymous_proxy
- **Galaxy**: https://galaxy.ansible.com/ui/standalone/roles/BestianCode/anonymous_proxy
