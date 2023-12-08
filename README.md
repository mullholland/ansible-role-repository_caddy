# [Ansible role repository_caddy](#repository_caddy)

Adds the caddy repository (https://caddyserver.com/docs/install) to your system

|GitHub|Downloads|Version|
|------|---------|-------|
|[![github](https://github.com/mullholland/ansible-role-repository_caddy/actions/workflows/molecule.yml/badge.svg)](https://github.com/mullholland/ansible-role-repository_caddy/actions/workflows/molecule.yml)|[![downloads](https://img.shields.io/ansible/role/d/mullholland/repository_caddy)](https://galaxy.ansible.com/mullholland/repository_caddy)|[![Version](https://img.shields.io/github/release/mullholland/ansible-role-repository_caddy.svg)](https://github.com/mullholland/ansible-role-repository_caddy/releases/)|
## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/mullholland/ansible-role-repository_caddy/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: Converge
  hosts: all
  become: true
  gather_facts: true
  vars:
    Key: Value
  roles:
    - role: "mullholland.repository_caddy"
```

The machine needs to be prepared. In CI this is done using [`molecule/default/prepare.yml`](https://github.com/mullholland/ansible-role-repository_caddy/blob/master/molecule/default/prepare.yml):

```yaml
---
- name: Prepare
  hosts: all
  become: true
  gather_facts: true

  tasks: []
  roles: []
```



## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/mullholland/ansible-role-repository_caddy/blob/master/defaults/main.yml):

```yaml
---
repository_caddy_gpg_key: "https://dl.cloudsmith.io/public/caddy/stable/gpg.key"
repository_caddy_keyring: "/etc/apt/trusted.gpg.d/caddy.gpg"
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/mullholland/ansible-role-repository_caddy/blob/master/requirements.txt).


## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://mullholland.net) for further information.

Here is an overview of related roles:
![dependencies](https://raw.githubusercontent.com/mullholland/ansible-role-repository_caddy/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/mullholland):

|container|tags|
|---------|----|
|[EL](https://hub.docker.com/r/mullholland/enterpriselinux)|all|
|[Amazon](https://hub.docker.com/r/mullholland/amazonlinux)|Candidate|
|[Fedora](https://hub.docker.com/r/mullholland/fedora/)|38, 39|
|[Ubuntu](https://hub.docker.com/r/mullholland/ubuntu)|all|
|[Debian](https://hub.docker.com/r/mullholland/debian)|all|

The minimum version of Ansible required is 2.10, tests have been done to:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them in [GitHub](https://github.com/mullholland/ansible-role-repository_caddy/issues).

## [License](#license)

[MIT](https://github.com/mullholland/ansible-role-repository_caddy/blob/master/LICENSE).

## [Author Information](#author-information)

[Mullholland](https://mullholland.net)
