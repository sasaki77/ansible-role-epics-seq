# Ansible Role: EPICS sequencer

Installs EPICS sequencer on RHEL/CentOS.

## Requirements

- ansible >= 2.3

## Role Variables
Refer to `defaults/main.yml` in detail.
```
epics_seq_module:
  name: "seq"
  type: "soft"
  ver: "2.2.4"
  url: "http://www-csr.bessy.de/control/SoftDist/sequencer/releases/seq-2.2.4.tar.gz"
  unarchived_name: "seq-2.2.4"
  configure_release:
      - {name: "EPICS_BASE", path: "{{ epics_base_base_name }}", reg: "^(.*)EPICS_BASE(.*)=(.*)$"}
```

## Dependencies

- [ansible-role-epics-base](https://github.com/sasaki77/ansible-role-epics-base)

## Example Playbook
```
- hosts: epics-base
  roles:
    - role: ansible-role-epics-base
    - role: ansible-role-epics-seq
```

## License

None.

## Author Information

This role was created by Shinya Sasaki.
