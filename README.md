# Ansible Role: Asciinema

[![Build Status](https://travis-ci.org/mtlynch/ansible-role-asciinema.svg?branch=master)](https://travis-ci.org/mtlynch/ansible-role-asciinema)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-asciinema-blue.svg?style=flat-square)](https://galaxy.ansible.com/mtlynch/asciinema)
[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](LICENSE)

Installs [Asciinema](https://asciinema.org) to Ubuntu/Debian systems.

## Role Variables

Available variables are listed below, along with default values (see [defaults/main.yml](defaults/main.yml)):

The location of the Asciinema config directory:

```yaml
asciinema_config_dir: "{{ ansible_env.HOME }}/.config/asciinema"
```

The Asciinema install ID (a GUID that authenticates Asciinema to an account):

```yaml
asciinema_install_id: null
```

## Dependencies

None

## Example Playbook

#### `example.yml`

```yaml
---
- hosts: all
  become: True
  become_method: sudo
  become_user: root
  roles:
    - role: mtlynch.asciinema
```

### Running Example Playbook

To run the example playbook, `example.yml` (above), run the following commands:

```shell
ansible-galaxy install mtlynch.asciinema
ansible-playbook example.yml
```

## License

MIT

## Author Information

This role was created in 2018 by [Michael Lynch](https://mtlynch.io).
