Role Name
=========

Installs Docker and `docker-py`.

Requirements
------------

None

Role Variables
--------------

```
docker_enabled: true
docker_opts: ""
```

Dependencies
------------

None

Example Playbook
----------------

    - name: servers
      vars:
        docker_opts: "--log-opt max-size=500m --log-opt max-file=3"
      roles:
        - {{ lmickh.docker }}

TODO
----

Greater distro support
Daemon config

License
-------

MIT
