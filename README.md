Role Name
=========

Manage /etc/security/limits.conf.

Requirements
------------

None

Role Variables
--------------

```
ulimit_config: []
```
Every element should contain a `domain`, `type`, `item`, and `value`.
See the limit.conf(5) man page for more details.  Example below.

Dependencies
------------

None

Example Playbook
----------------

    - hosts: some_servers
      vars:
        ulimit_config:
         - domain: 'johndoe'
           type: hard
           item: nofile
           value: 400
      roles:
        - {{ lmickh.ulimit }}

License
-------

MIT
