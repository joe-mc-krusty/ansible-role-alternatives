Ansible Role: Alternatives
=========

A Role for managing Alternatives

** co-maintainers welcome **

Requirements
------------

Update-alternatives must be available (alternatives package)
This missing dependency will be addressed in the future within the role itself.

See TODO section of README.

Role Variables
--------------

```yaml
alternatives:
  - name: python
    path: /usr/bin/python3
    link: /usr/bin/python # optional

  - name: hadoop-conf
    link: /etc/hadoop/conf
    path: /etc/hadoop/conf.ansible
  
  - name: java
    path: /usr/lib/jvm/java-7-openjdk-i386/jre/bin/java
    priority: -10 # optional - default = 50
```

Dependencies
------------

None

Example Playbook
----------------

```yaml
    - hosts: servers
      roles:
         - joe_mc_krusty.alternatives
    
    # OR

    - hosts: servers
      tasks:
        - include_role:
            name: joe_mc_krusty.alternatives
```

TODO
----
- Check for alternatives tool installation on any OS

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
