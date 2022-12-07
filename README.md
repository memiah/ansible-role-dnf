Role Name
=========

Install and configure dnf-automatic on hosts which use the dnf package manager. A possible use case is the automatic installation of security updates.

See https://dnf.readthedocs.org/en/latest/automatic.html for more information about dnf-automatic.

Requirements
------------

In order for Ansible to work (on Fedora based hosts), it is necessary to have the packages python2, python2-dnf and libselinux-python installed.

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

    dnf_automatic_enabled: True
    
    dnf_automatic_upgrade_type: security
    dnf_automatic_apply_updates: yes
    dnf_automatic_random_sleep: 300
    dnf_automatic_download_updates: yes
    dnf_automatic_email_from: root@example.com
    dnf_automatic_email_to: root

This default configuration sets dnf-automatic up to automatically download and install only security updates.

Dependencies
------------

No dependencies needed.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - memiah.dnf

License
-------

MIT / BSD

Author Information
------------------

This role was created in 2022 by [Memiah Limited](https://github.com/memiah).
