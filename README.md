sudo-pair
=========

[![Build Status](https://travis-ci.org/robertdebock/ansible-role-sudo-pair.svg?branch=master)](https://travis-ci.org/robertdebock/ansible-role-sudo-pair)

Provides sudo-pair for your system.

Context
-------
This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://robertdebock.nl/) for further information.

Here is an overview of related roles:
![dependencies](https://raw.githubusercontent.com/robertdebock/drawings/artifacts/sudo-pair.png "Dependency")

Requirements
------------

Access to a repository containing packages, likely on the internet.

Role Variables
--------------

- sudo_pair_version:
- sudo_pair_gids_enforced: 0
- sudo_pair_gids_exempted: none

Dependencies
------------

This role can be used to prepare your system:

- [robertdebock.bootstrap](https://travis-ci.org/robertdebock/ansible-role-bootstrap)
- [robertdebock.epel](https://travis-ci.org/robertdebock/ansible-role-epel)
- [robertdebock.buildtools](https://travis-ci.org/robertdebock/ansible-role-buildtools)
- [robertdebock.cargo](https://travis-ci.org/robertdebock/ansible-role-cargo)

Download the dependencies by issuing this command:
```
ansible-galaxy install --role-file requirements.yml
```

Compatibility
-------------

This role has been tested against the following distributions and Ansible version:

|distribution|ansible 2.4|ansible 2.5|ansible 2.6|
|------------|-----------|-----------|-----------|
|alpine-edge|no|no|no|
|alpine-latest|no|no|no|
|archlinux|yes|yes|yes|
|centos-6|no|no|no|
|centos-latest|yes|yes|yes|
|debian-latest|yes|yes|yes|
|debian-stable|yes|yes|yes|
|fedora-latest|yes|yes|yes|
|fedora-rawhide|yes|yes|yes|
|opensuse-leap|yes|yes|yes|
|opensuse-tumbleweed|yes|yes|yes|
|ubuntu-artful|yes|yes|yes|
|ubuntu-latest|yes|yes|yes|

Example Playbook
----------------

The simplest way possible:
```
- hosts: servers

  roles:
    - robertdebock.bootstrap
    - robertdebock.buildtools
    - robertdebock.sudo-pair
```

Install this role using `galaxy install robertdebock.sudo-pair`.

License
-------

Apache License, Version 2.0

Author Information
------------------

[Robert de Bock](https://robertdebock.nl/) <robert@meinit.nl>
