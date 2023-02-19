Role Name
=========

Setup and configure an NFS server by exporting user defined export statements

Requirements
------------

No external dependency or requirement for this role.

Role Variables
--------------

```
nfs_exports
```
nfs_exports holds an array of exports that this NFS server will be configured with. example
```
/srv/homes       hostname1(rw,sync,no_subtree_check)
```

```
rpcbind_state: started
rpcbind_enabled: true
```
Applicable for RedHat/CentOS/Fedora and rpcbind options will define the state of this service at the time of system boot

Example Playbook
----------------

```
- hosts: target
  roles:
    - { role: anuragjain_ca.nfs }
```

License
-------

BSD

Author Information
------------------

Anurag Jain, Developer Advocate, Thales