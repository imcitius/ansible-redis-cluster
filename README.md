redis-cluster.role
=========

This role configures redis cluster, using redis-sentinel.
By default haproxy will listen default redis's port 6379, and route traffic to master server.
Redis instances will listen and recieve clients's traffic via haproxy on port 16379.

This role is based on davidwittman.redis role, and rewritten to dynamically detect master/slave servers role.

Role Variables
--------------

# whether to disable Transparent Huge pages as per redis recommendation
thp_disable: true

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - { role: redis-cluster.role }

License
-------

GPLv2

Author Information
------------------

Ilya Rubinchik, a.k.a. Citius
