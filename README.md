GITLAB
=========
Deploy the gitlab server running under the container via ansible.

Dependencies
------------

- [Docker](https://github.com/gengxiankun-galaxy/docker)

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
         - gengxiankun.gitlab

License
-------

BSD

Author Information
------------------

This role was created in 2019 by Xiankun Geng, Learn more about the author's role in [galaxy](https://galaxy.ansible.com/gengxiankun).
