
An [ansible](http://ansibleworks.com) role for install [supervisor](http://supervisord.org/) on CentOS, and add init script for running `supervisord` automatically on startup. Only tested on CentOS 6.x currently.

It forks and changes from [ansible-supervisor](https://github.com/eggsby/ansible-supervisor). Init script comes from [Supervisor initscripts](https://github.com/Supervisor/initscripts).



Role Variables
--------------

```
supervisor_conf: '/etc/supervisord.conf'
supervisor_conf_dir: '/etc/supervisord.d'
supervisor_pidfile: '/tmp/supervisord.pid'
supervisor_logfile: '/tmp/supervisord.log'

supervisor_http: off
supervisor_http_host: 127.0.0.1
supervisor_http_port: 9001

supervisor_http_auth: off
# supervisor_http_auth:
#   username: foo
#   password: bar

```



Example Playbook
----------------

    - hosts: servers
      roles:
        - role: semparatus.supervisor2


License
-------

MIT
