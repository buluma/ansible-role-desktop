# [desktop](#desktop) [ARCHIVED]
==================

Note: This repository has been archived, no maintenance is being performed anymore. It's been replaced by [ansible-role-gnome](https://github.com/buluma/ansible-role-gnome), [ansible-role-mate](https://github.com/buluma/ansible-role-mate) and [ansible-role-i3](https://github.com/buluma/ansible-role-gnome).

Install one of the many desktop environments.

|GitHub|GitLab|Quality|Downloads|Version|Issues|Pull Requests|
|------|------|-------|---------|-------|------|-------------|
|[![github](https://github.com/buluma/ansible-role-desktop/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-desktop/actions)|[![gitlab](https://gitlab.com/shadowwalker/ansible-role-desktop/badges/master/pipeline.svg)](https://gitlab.com/shadowwalker/ansible-role-desktop)|[![quality](https://img.shields.io/ansible/quality/58800)](https://galaxy.ansible.com/buluma/desktop)|[![downloads](https://img.shields.io/ansible/role/d/58800)](https://galaxy.ansible.com/buluma/desktop)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-desktop.svg)](https://github.com/buluma/ansible-role-desktop/releases/)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-desktop.svg)](https://github.com/buluma/ansible-role-desktop/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-desktop.svg)](https://github.com/buluma/ansible-role-desktop/pulls/)|

## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/buluma/ansible-role-desktop/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: Converge
  hosts: all
  become: yes
  gather_facts: yes

  roles:
    - role: buluma.desktop
      desktop: gnome
```

The machine needs to be prepared. In CI this is done using [`molecule/default/prepare.yml`](https://github.com/buluma/ansible-role-desktop/blob/master/molecule/default/prepare.yml):

```yaml
---
- name: Converge
  hosts: all
  become: yes
  gather_facts: no

  roles:
    - role: buluma.bootstrap
```

Also see a [full explanation and example](https://buluma.github.io/how-to-use-these-roles.html) on how to use these roles.

## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/buluma/ansible-role-desktop/blob/master/defaults/main.yml):

```yaml
---
# defaults file for desktop

# What desktop to use. Either "gnome", "i3" or "mate"
desktop: gnome
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-desktop/blob/master/requirements.txt).

## [State of used roles](#state-of-used-roles)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | GitLab |
|-------------|--------|--------|
|[buluma.bootstrap](https://galaxy.ansible.com/buluma/bootstrap)|[![Build Status GitHub](https://github.com/buluma/ansible-role-bootstrap/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-bootstrap/actions)|[![Build Status GitLab](https://gitlab.com/shadowwalker/ansible-role-bootstrap/badges/master/pipeline.svg)](https://gitlab.com/shadowwalker/ansible-role-bootstrap)|

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-desktop/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|[EL](https://hub.docker.com/repository/docker/buluma/enterpriselinux/general)|7|
|[Fedora](https://hub.docker.com/repository/docker/buluma/fedora/general)|all|
|[Ubuntu](https://hub.docker.com/repository/docker/buluma/ubuntu/general)|all|

The minimum version of Ansible required is 2.7, tests have been done to:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them in [GitHub](https://github.com/buluma/ansible-role-desktop/issues)

## [Changelog](#changelog)

[Role History](https://github.com/buluma/ansible-role-desktop/blob/master/CHANGELOG.md)

## [License](#license)

[Apache-2.0](https://github.com/buluma/ansible-role-desktop/blob/master/LICENSE).

## [Author Information](#author-information)

[buluma](https://buluma.github.io/)

Please consider [sponsoring me](https://github.com/sponsors/buluma).

### [Special Thanks](#special-thanks)

Template inspired by [Robert de Bock](https://github.com/robertdebock)
