# Base Ansible Role

An Ansible role to install and reconfigure default packages on a system.

## Features
- Installs essential packages.
- Configures default settings for installed packages.
- Provides flexibility through variables for customization.

## Requirements
- Ansible 2.9 or higher.
- Supported platforms:
  - **Debian-based systems:** Debian, Ubuntu.

## Role Variables
The following variables can be customized in your playbook or via extra-vars:

### Defaults
Located in `defaults/main.yml`:
```yaml
# Example variable definitions
# defaults file for base
defaults_prerequisites_packages:
  - curl
  - wget
  - unzip
  - net-tools
  - dnsutils
  - apt-transport-https
  - gnupg2
  - lsb-release
```
Example playbook:
```yaml
# Example playbook
---
- name: Install base packages
  hosts: all
  become: yes
  gather_facts: yes

  roles:
  - base
```
## Dependencies
None.

## License
MIT

## Author Information
This role was created by Chakib. Contributions and feedback are welcome!