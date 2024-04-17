# Role Description

This Ansible role installs and configures an anonymous proxy server on a FreeBSD or Linux server.

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

## URLs

- **GitHub**: https://github.com/BestianCode/ansible.role.anonymous_proxy
##- **Galaxy**: https://galaxy.ansible.com/ui/repo/published/bestiancode/sysadmin
