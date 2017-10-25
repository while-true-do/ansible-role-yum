# Ansible Role: yum 
| A role to configure yum

## Installation

Galaxy Link: <https://galaxy.ansible.com/while-true-do/yum>

```
ansible-galaxy install while-true-do.yum
```

Github Link: <https://github.com/while-true-do/ansible-role-yum>

```
git clone https://github.com/while-true-do/ansible-role-yum.git while-true-do.yum
```

## Requirements

None.

## Dependencies

None.

## Role Variables
Please see 'man yum.conf' to see possible options.

```
# defaults/main.yml
yum_packages: [ 'yum', 'yum-langpacks', 'yum-plugin-fastestmirror' ]

yum_cachedir: '/var/cache/yum/$basearch/$releasever'
yum_keepcache: '0'
yum_debuglevel: '2'
yum_logile: '/var/log/yum.log'
yum_exactarch: '1'
yum_obsoletes: '1'
yum_gpgcheck: '1'
yum_plugins: '1'
yum_installonly_limit: '5'
yum_bugtracker_url: 'http://bugs.centos.org/set_project.php?project_id=23&ref=http://bugs.centos.org/bug_report_page.php?category=yum'
yum_distroverpkg: 'centos-release'
yum_clean_requirements_on_remove: 'yes'
yum_metadata_expire: '90m'
```

## Example Playbook

Simple Example:

```
- hosts: servers 
  roles:
    - { role: while-true-do.yum }
```

## License

This work is licensed under a [BSD License](https://opensource.org/licenses/BSD-3-Clause).

## Contribute / Bugs

**bug reports:** <https://github.com/while-true-do/ansible-role-yum/issues>

**contributers:** <https://github.com/while-true-do/ansible-role-yum/graphs/contributors>

## Author Information

**blog:** <https://blog.while-true-do.org>

**github:** <https://github.com/daniel-wtd>

**contact:** [mail@while-true-do.org](mailto:mail@while-true-do.org)
