# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## Unreleased

### Removed

- Remove compatibility with Ansible 2.9 and lower.

## [1.2.1] - 2022-01-27

### Fixed

- Fix deprecation warning wording.

## [1.2.0] - 2022-01-20

### Deprecated

- Deprecate specifying datasets and templates as dictionary.

## [1.1.0] - 2022-01-06

### Added

- Add new format for specifying datasets and templates. It fixes the problem of using
characters illegal for Ansible variables in your dataset and template names.

## 1.0.0 - 2020-12-17

### Added

- First public version.

[1.1.0]: https://gitlab.com/radek-sprta/ansible-role-node-exporter/compare/v1.0.0...v1.1.0
[1.2.0]: https://gitlab.com/radek-sprta/ansible-role-node-exporter/compare/v1.1.0...v1.2.0
[1.2.1]: https://gitlab.com/radek-sprta/ansible-role-node-exporter/compare/v1.2.0...v1.2.1
