ansible-h2o
=========

install h2o webserver

Requirements
------------

None.

Role Variables
--------------

# defaults file for h2o
- h2o_src: /usr/local/src

- h2o_var: /var/h2o
- h2o_doc: /var/h2o/doc
- h2o_logs: /var/h2o/logs
- h2o_conf: /var/h2o/conf

#vars file for h2o
h2o_yum_packages:
 - cmake
 - openssl-devel
 - libyaml-devel

h2o_makedir:
 - "{{ h2o_src }}"
 - "{{ h2o_var }}"
 - "{{ h2o_doc }}"
 - "{{ h2o_logs }}"
 - "{{ h2o_conf }}"

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - h2o

Start and stop h2o
------------------

/etc/init.d/h2o start
/etc/init.d/h2o stop

License
-------

MIT

Author Information
------------------
Twitter: @kazu20
