Syncthing
=========

Installs and configures Syncthing for the user.

Requirements
------------

The following collections are required:

- community.general

They can be installed by running `ansible-galaxy collection install $COLLECTION`.

To include this role in your `requirements.yml` file, add the following list item:

```yaml
---
roles:
  - name: whalej84.syncthing
    src: https://github.com/WhaleJ84/ansible-role-syncthing.git
    scm: git

  - name: whalej84.lxml
    src: https://github.com/WhaleJ84/ansible-role-lxml.git
    scm: git

collections:
  - community.general
```

Role Variables
--------------

| Name | Type | Description | Default |
| ---- | ---- | ----------- | ------- |
| syncthing\_config\_dir | string | A path to state where the syncthing config file should be located | "$HOME/.config/syncthing" |
| minumum\_free\_disk\_percentage | string | A numeric value to state the minimum percent of free disk space required for shared folders | 15 |

Example Playbook
----------------

This example playbook shows how I would use this role, with custom variables to suit my needs.

```yaml
---
- hosts: localhost
  
  roles:
    role: whalej84.syncthing
    tags: [ syncthing ]
```

