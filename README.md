GITLAB
=========
Deploy the gitlab server running under the container via ansible.

Installation
------------

`ansible-galaxy install gengxiankun.gitlab`

Dependencies
------------

- [Docker](https://github.com/gengxiankun-galaxy/docker)

Role Variables
--------------

parameter | description
------------ | -------------
SRV_PATH | 持久化目录
GITLAB_HOSTNAME | GitLab hostname
GITLAB_EXTERNAL_URL | GitLab external url
GITLAB_HTTP_PORT | HTTP端口号
GITLAB_SSH_PORT | SSH端口号
GITLAB_REGISTRY_ENABLED | registry_enabled
GITLAB_REGISTRY_EXTERNAL_URL | registry_external_url
GITLAB_REGISTRY_HOST | registry_host
GITLAB_REGISTRY_PORT | registry_port
REGISTRY_PATH | registry_path
GITLAB_REGISTRY_API_URL | registry_api_url

Example Playbook
----------------

    - hosts: servers
      roles:
        - gengxiankun.gitlab
      vars:
      	    OPT_PATH: '/opt/gengxiankun-galaxy'
	    SRV_PATH: '/data/srv'
	    GITLAB_HOSTNAME: 'gitlab.example.com'
	    GITLAB_EXTERNAL_URL: 'http://gitlab.example.com'
	    GITLAB_HTTP_PORT: 80
	    GITLAB_SSH_PORT: 2222
	    GITLAB_REGISTRY_ENABLED: true
	    GITLAB_REGISTRY_EXTERNAL_URL: 'http://registry.example.com:5005'
	    GITLAB_REGISTRY_HOST: 'registry.gitlab.example.com'
	    GITLAB_REGISTRY_PORT: '5005'
	    REGISTRY_PATH: '{{ SRV_PATH }}/registry'
	    GITLAB_REGISTRY_API_URL: 'http://:5000'


License
-------

BSD

Author Information
------------------

This role was created in 2019 by Xiankun Geng, Learn more about the author's role in [galaxy](https://galaxy.ansible.com/gengxiankun).
