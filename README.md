[![Build Status](https://travis-ci.org/while-true-do/ansible-role-yum.svg?branch=master)](https://travis-ci.org/while-true-do/ansible-role-yum)

# Ansible Role: yum 
| A role to configure yum

## Motivation

Configuring and ensuring a proper behaviour of yum on CentOS/RedHat systems is mandatory.

## Installation

Install from [Ansible Galaxy](https://galaxy.ansible.com/while-true-do/yum)

```
ansible-galaxy install while-true-do.yum
```

Install from [Github](https://github.com/while-true-do/ansible-role-yum)

```
git clone https://github.com/while-true-do/ansible-role-yum.git while-true-do.yum
```

## Requirements

None.

## Dependencies

None.

## Role Variables

```
# defaults/main.yml
wtd_yum_packages: [ 'yum', 'yum-utils', 'deltarpm', 'yum-langpacks', 'yum-plugin-fastestmirror' ]

wtd_yum_cachedir: '/var/cache/yum/$basearch/$releasever'
wtd_yum_keepcache: '0'
wtd_yum_debuglevel: '2'
wtd_yum_logfile: '/var/log/yum.log'
wtd_yum_exactarch: '1'
wtd_yum_obsoletes: '1'
wtd_yum_gpgcheck: '1'
wtd_yum_plugins: '1'
wtd_yum_installonly_limit: '5'
wtd_yum_bugtracker_url: 'http://bugs.centos.org/set_project.php?project_id=23&ref=http://bugs.centos.org/bug_report_page.php?category=yum'
wtd_yum_distroverpkg: 'centos-release'
wtd_yum_clean_requirements_on_remove: 'yes'
wtd_yum_metadata_expire: '90m'
```

## Example Playbook

Simple Example:

```
- hosts: servers 
  roles:
    - { role: while-true-do.yum }
```

## Testing

All tests are located in [test directory](./tests/).

Basic testing:

```
bash ./tests/test-spelling.sh
bash ./tests/test-ansible.sh
```

## Contribute / Bugs

Thank you so much for considering to contribute. Every contribution helps us.
We are really happy, when somebody is joining the hard work. Please have a look
at the links first.

-   [Contribution Guidelines](./docs/CONTRIBUTING.md)
-   [Create an issue or Request](https://github.com/while-true-do/ansible-role-yum/issues)
-   [See who was contributing already](https://github.com/while-true-do/ansible-role-yum/graphs/contributors)

## License

This work is licensed under a [BSD License](https://opensource.org/licenses/BSD-3-Clause).

## Author Information

Blog: [blog.while-true-do.org](https://blog.while-true-do.org)

Mail: [hello@while-true-do.org](mailto:hello@while-true-do.org)
