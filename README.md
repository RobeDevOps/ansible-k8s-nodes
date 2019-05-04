robedevops.ansible_k8s_nodes
=========

This Role installs and configures all the packages and files required by a node in order to be part of the cluster.

Requirements
------------

N/A

Role Variables
--------------

N/A

Dependencies
------------

There is not dependency with other roles by I recommend to use **robedevops.ansible_docker** and **robedevops.ansible_docker_user** with this role. (I always used in that way but that is not required)

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
    - hosts: nodes
      roles:
         - { role: robedevops.ansible_k8s_node }
```

License
-------

BSD

Author Information
------------------

Roberto Cardenas Isla - email: rcardenas20@gmail.com