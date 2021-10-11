# Changelog

All notable changes to this project will be documented in this file.

- [2.0.0 (2021-10-11)](#200-2021-10-11)
- [1.2.2 (2020-05-28)](#122-2020-05-28)
- [1.2.1 (2020-05-18)](#121-2020-05-18)
- [1.2.0 (2020-05-18)](#120-2020-05-18)
- [1.1.0 (2020-03-22)](#110-2020-03-22)
- [1.0.1 (2020-03-22)](#101-2020-03-22)
- [1.0.0 (2020-03-19)](#100-2020-03-19)

---

<a name="2.0.0"></a>
## [2.0.0](https://github.com/aisbergg/ansible-role-btrfsmaintenance/compare/v1.2.2...v2.0.0) (2021-10-11)

### CI Configuration

- add Github action for automatic releases

### Chores

- update changelog
- update development configs
- **.pre-commit-config.yaml:** bump pre-commit hook versions
- **CHANGELOG.tpl.md:** update changelog template

### Code Refactoring

- drop support for Ansible < 2.10


<a name="1.2.2"></a>
## [1.2.2](https://github.com/aisbergg/ansible-role-btrfsmaintenance/compare/v1.2.1...v1.2.2) (2020-05-28)

### Code Refactoring

- clean up repo


<a name="1.2.1"></a>
## [1.2.1](https://github.com/aisbergg/ansible-role-btrfsmaintenance/compare/v1.2.0...v1.2.1) (2020-05-18)

### Bug Fixes

- narrow down supported platforms


<a name="1.2.0"></a>
## [1.2.0](https://github.com/aisbergg/ansible-role-btrfsmaintenance/compare/v1.1.0...v1.2.0) (2020-05-18)

### Code Refactoring

- add checkmode and cleanup


<a name="1.1.0"></a>
## [1.1.0](https://github.com/aisbergg/ansible-role-btrfsmaintenance/compare/v1.0.1...v1.1.0) (2020-03-22)

### Bug Fixes

- installation
- use bash explicitly, so the role won't fail on Ubuntu

### Chores

- update changelog
- update changelog

### Features

- reload the systemd daemon config after install


<a name="1.0.1"></a>
## [1.0.1](https://github.com/aisbergg/ansible-role-btrfsmaintenance/compare/v1.0.0...v1.0.1) (2020-03-22)

### Bug Fixes

- correct Ansible required version
- use sort -V for sorting versions

### Chores

- update changelog


<a name="1.0.0"></a>
## [1.0.0]() (2020-03-19)

### Bug Fixes

- set the default state to stopped, so that the task doesn't change all the time
- linting errors
- typo

