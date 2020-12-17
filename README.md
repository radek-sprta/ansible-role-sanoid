# Ansible Role: Sanoid [![Ansible Role](https://img.shields.io/ansible/role/projectId)](https://galaxy.ansible.com/radek_sprta/sanoid) [![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/radek-sprta/ansible-role-sanoid)](https://gitlab.com/radek-sprta/ansible-role-sanoid/-/tags) [![Ansible Role](https://img.shields.io/ansible/role/d/projectId)](https://galaxy.ansible.com/radek_sprta/sanoid) [![Ansible Role](https://img.shields.io/ansible/quality/projectId)](https://galaxy.ansible.com/radek_sprta/sanoid) [![Pipeline status](https://gitlab.com/radek-sprta/ansible-role-sanoid/badges/master/pipeline.svg)](https://gitlab.com/radek-sprta/ansible-role-sanoid/commits/master)

Install and configure Sanoid for automatic ZFS snapshots.

## Role Variables

List of variables from `defaults/main.yml`.

```yaml
sanoid_package: sanoid
```

Package to install. You should not need to override this.

```yaml
sanoid_templates:
  example:
    frequently: 0
    hourly: 24
    daily: 7
    monthly: 12
    yearly: 0
    autosnap: "yes"
    autoprune: "yes"
```

Dictionary of Sanoid backup templates. The example showcases available options. The quotes around "yes" are required.

```yaml
sanoid_datasets:
  example:
    use_template: example
    recursive: "yes"
    process_children_only: "yes"
    yearly: 1
```

Dictionary of datasets to take snapshots of. The example showcases some of the available options. In addition, options from sanoid\_templates are available as well. The quotes around "yes" are required.

## Example Playbook

```yaml
- hosts: all

  vars:
    tank:
      process_children_only: "yes"
      recursive: "yes"
      use_template: example

  roles:
     - radek_sprta.sanoid
```

## License

MIT

## Author Information

Radek Sprta <mail@radeksprta.eu>
