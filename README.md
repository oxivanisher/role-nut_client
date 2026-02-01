nut_client
==========
[![Ansible Lint](https://github.com/oxivanisher/role-nut_client/actions/workflows/ansible-lint.yml/badge.svg)](https://github.com/oxivanisher/role-nut_client/actions/workflows/ansible-lint.yml)

This role configures a nut client for UPS monitoring.


Requirements
------------

A configured nut server.

Role Variables
--------------


| Name                 | Comment                                        | Default value |
| -------------------- | ---------------------------------------------- | ------------- |
| nut_client_server    | IP or hostname of the nut server               | `localhost`   |
| nut_client_ups       | The name of the USV (configured in nut server) | `qnapups`     |
| nut_client_user      | Nut server user                                | `nutclient`   |
| nut_client_password  | Nut server password                            | ``            |
| nut_client_force_ssl | Force SSL 1/0                                  | `0`           |

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- name: Configure nut client
  hosts: rack
  collections:
    - oxivanisher.linux_base
  roles:
    - role: oxivanisher.linux_base.nut_client
```

License
-------

BSD

Author Information
------------------

This role is part of the [oxivanisher.linux_base](https://galaxy.ansible.com/ui/repo/published/oxivanisher/linux_base/) collection, and the source for that is located on [github](https://github.com/oxivanisher/collection-linux_base).
