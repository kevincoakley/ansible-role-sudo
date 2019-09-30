ansible-role-sudo
=================

[![Build Status](https://travis-ci.org/kevincoakley/ansible-role-sudo.svg?branch=master)](https://travis-ci.org/kevincoakley/ansible-role-sudo)

Manage sudos for CentOS 7 and Ubuntu 18.04

Requirements
------------

None

Role Variables
--------------

See defaults/main.yml

Dependencies
------------

None

Example Playbook
----------------

    - sudo:
        - username: user1
          permissions:
            - host: localhost
              runas: root
              nopasswd: true
              command: /bin/bash
            - nopasswd: false
              command: /bin/whoami
        - username: user2
          permissions:
            - command: ALL
            - command: /bin/bash
              state: absent


License
-------

BSD

Author Information
------------------

Kevin Coakley (https://github.com/kevincoakley)