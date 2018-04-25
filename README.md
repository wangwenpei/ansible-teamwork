Ansible-Teamwork
============================================================================================

Manage Your team member permission use ansible.
It is useful when your teamwork treat "a team" as atomic unit to assign machine resource in a large team.


Install
-------

```
ansible-galaxy install wangwenpei.teamwork
```

Role Variables
--------------

```
pubkey_path: ./files/keys
pubkey_departing_path: ./files/departing-keys

```

How to
-----

- add member keys in your $pubkey_path
- add your free machine in free file
- edit hosts file

```

[wangwenpei]
192.168.1.1  refund=yes # if you want to refund/release your machine

```



Example Playbook
----------------

For target machine

```
    - hosts: servers
      roles:
        - wangwenpei.teamwork
```


License
-------

GPLv3

Author Information
------------------

Author: wangwenpei
