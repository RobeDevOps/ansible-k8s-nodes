robedevops.ansible_k8s_nodes
=========

This Role installs and configures all the packages and files required by a node in order to be part of the cluster:

* Set setenforce to zero
* Disable SELINUX
* Ensure modprobe br_netfilter
* Enable iptables forward
* Add kubernetes repositories
* Install the packages: kubelet, kubeadm, kubectl

Requirements
------------

Python is required in order to use ansible module **yum**

Role Variables
--------------

N/A (working on multiple platforms and then define the variables)

Dependencies
------------

There is not dependency with other roles by I recommend to use **robedevops.ansible_docker** and **robedevops.ansible_docker_user** with this role. (I always used in that way but that is not required)

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: k8s-nodes
  gather_facts: yes
  become: yes
  roles:
    - { role: robedevops.ansible_docker, tags: ['docker'] }
    - { role: robedevops.ansible_docker_user, tags: ['docker-user'] }
    - { role: robedevops.ansible_k8s_nodes, tags: ['k8s-nodes'] }
```

License
-------

BSD

Author Information
------------------

Roberto Cardenas Isla - email: rcardenas20@gmail.com