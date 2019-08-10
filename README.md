Ansible Role: AWSCLI
=========

[![Build Status](https://travis-ci.org/kotarella1110/ansible-role-awscli.svg?branch=master)](https://travis-ci.org/kotarella1110/ansible-role-awscli)

This role to manage awscli users.

Requirements
------------

None.

Role Variables
--------------

```
awscli_users:
  # Add the user 'johnd'
  - name: johnd
    state: present
    configure:
      - profile: default
        aws_access_key_id: XXXXXXXXXXXXXXXXXXXX
        aws_secret_access_key: XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
        output: json
        region: ap-northeast-1
  # Remove the user 'johnd'
  - name: johnd
    state: absent
```

Dependencies
------------

None.

Example Playbook
----------------

```
- hosts: servers
  roles:
     - { role: dzangolab.awscli }
```

License
-------

MIT

Author Information
------------------

Forked from `kotarella1110/awscli` role originally created in 2016 by Kotaro Sugawara.
