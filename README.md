gitlab
=========

Requirements
------------

CENTOS 7+

Role Variables
--------------

parameter | description
------------ | -------------
SRV_PATH | 持久化目录
GITLAB_HOSTNAME |  
GITLAB_EXTERNAL_URL | 
GITLAB_HTTP_PORT | HTTP端口号
GITLAB_SSH_PORT | SSH端口号


Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: gitlab }

License
-------

BSD
