ansible-role-nfs-server
=========

This roles setup nfs server. Role is very simple. If something is missing let us know.


Role Variables
--------------

All default variables are predefined in defaults/main.yml.

### Cron Jobs

We added possibility to run some cron jobs that could be useful for some standard nfs orchestration like, backup, cleaning or archiving. They are using standard cron notation:

```
* * * * * command to execute
| | | | |- day of week - attribute: weekday, default (*)
| | | |- month - attribute: month, default (*)
| | |- day of month - attribute: day, default (*)
| |- hour - attribute: hour, default (0)
|- min - attribute: minute default (0)
```

Attributes `user` and `state` could be omit. Base on Ansible design you have to change the `state` from `present` to `absent` and rerun job before you remove cron job from inventory. 

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```bash
---
- hosts: localhost
  roles:
    - novomatic-tech.nfs_server
```

License
-------

MIT

Author Information
------------------

This role was created in 2019 for Novomatic Technologies Poland purposes.
