Docker
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
        docker_conf:
          log-driver: "json-file"
          log-opts:
            max-size: "250m"
            max-file: "5"
          live-restore: true
          max-concurrent-downloads: 10
          storage-driver: "overlay2"
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
