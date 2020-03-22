# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.1.0] - 2020-03-22
### Fixed
- Fix installation routine
- Execution on Ubuntu, where the shell scripts get executed with `sh` by default instead of `bash`
- Reload the systemd daemon, so the new installed service will be found

## [1.0.1] - 2020-03-22
### Changed
- Correct required Ansible version

### Fixed
- Use `sort -V` instead of the Git built-in feature to sort version tags

## [1.0.0] - 2020-02-19
### Added
- First version of the role
