Ansible Role: Podman
====================

[![molecule](https://github.com/diodonfrost/ansible-role-podman/workflows/molecule/badge.svg)](https://github.com/diodonfrost/ansible-role-podman/actions)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-diodonfrost.podman-660198.svg)](https://galaxy.ansible.com/diodonfrost/podman)

An Ansible Role that installs Podman on Linux.

Requirements
------------

None.

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

    # A list of users who will be used podman.
    rootless_users: []

Dependencies
------------

None.

Example Playbook
----------------

This is a sample playbook file for deploying the Ansible Galaxy podman role and installing podman.

    - hosts: all
      roles:
         - diodonfrost.podman

Local Testing
-------------

This project uses [Molecule](http://molecule.readthedocs.io/) to aid in the
development and testing.

To develop or test you'll need to have installed the following:

* Linux (e.g. [Ubuntu](http://www.ubuntu.com/))
* [Docker](https://www.docker.com/)
* [Python](https://www.python.org/) (including python-pip)
* [Ansible](https://www.ansible.com/)
* [Molecule](http://molecule.readthedocs.io/)

### Testing with Docker ###

```shell
# Test ansible role with centos 8
molecule test

# Test ansible role with ubuntu 20.04
image=ansible-ubuntu:20.04 molecule test

# Test ansible role with alpine latest
image=ansible-alpine:rolling molecule test

# Create centos 8 instance
molecule create

# Apply role on centos 8 instance
molecule converge

# Launch tests on centos 8 instance
molecule verify
```

License
-------

Apache 2.0

Author Information
------------------

This role was created in 2020 by diodonfrost.
