dudefellah.postfix
=========

A very simple Postfix installation and configuration role. Created since there
didn't seem to be anything very flexible for RHEL systems.

Requirements
------------

None.

Role Variables
--------------

See [defaults/main.yml](defaults/main.yml) for all values and associated
documentation for this role.

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: mailservers
      tasks:
        - name: Install and Configure Postfix
          include_role: dudefellah.postfix
          vars:
            postfix_configs:
              main.cf: |
                compatibility_level = 2
                queue_directory = /var/spool/postfix
                ...
            postfix_aliases:
              - name: bob
                values:
                  - robert
                  - rob
            ...

License
-------

GPLv2+

Author Information
------------------

Dan - github.com/dudefellah
