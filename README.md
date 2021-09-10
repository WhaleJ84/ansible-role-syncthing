Syncthing
=========

Installs and configures Syncthing for the user.

Requirements
------------

The following collections are required:

- community.general

They can be installed by running `ansible-galaxy collection install $COLLECTION`.

Role Variables
--------------

- syncthing\_config\_dir: $HOME/.config/syncthing
- minumum\_free\_disk\_percentage: 15

Example Playbook
----------------

    - hosts: localhost
      roles:
         - { role: whalej84.syncthing, minimum_free_disk_percentage: 10 }

