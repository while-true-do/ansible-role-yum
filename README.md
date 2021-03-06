[![Build Status](https://travis-ci.org/while-true-do/ansible-role-yum.svg?branch=master)](https://travis-ci.org/while-true-do/ansible-role-yum)

# Ansible Role: yum
| A role to configure yum

## Motivation

Configuring and ensuring a proper behaviour of yum on CentOS/RedHat systems is mandatory.

## Installation

Install from [Ansible Galaxy](https://galaxy.ansible.com/while_true_do/yum)

```
ansible-galaxy install while_true_do.yum
```

Install from [Github](https://github.com/while-true-do/ansible-role-yum)

```
git clone https://github.com/while-true-do/ansible-role-yum.git while_true_do.yum
```

## Requirements

Used Modules:

-   [command_module](https://docs.ansible.com/ansible/latest/modules/command_module.html)
-   [package_module](https://docs.ansible.com/ansible/latest/modules/package_module.html)
-   [template_module](https://docs.ansible.com/ansible/latest/modules/template_module.html)

## Dependencies

None.

## Role Variables

```yaml
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

```yaml
- hosts: servers
  roles:
    - { role: while_true_do.yum }
```

## Testing

All tests are located in [test directory](./tests/).

Basic testing:

```
bash ./tests/test-ansible.sh
bash ./tests/test-spelling.sh
bash ./tests/test-whitespace.sh
```

## Contribute / Bugs

Thank you so much for considering to contribute. Every contribution helps us.
We are really happy, when somebody is joining the hard work. Please have a look
at the links first.

-   [Code of Conduct](./docs/CODE_OF_CONDUCT.md)
-   [Contribution Guidelines](./docs/CONTRIBUTING.md)
-   [Create an issue or Request](https://github.com/while-true-do/ansible-role-yum/issues)
-   [See who was contributing already](https://github.com/while-true-do/ansible-role-yum/graphs/contributors)

## License

This work is licensed under a [BSD License](https://opensource.org/licenses/BSD-3-Clause).

## Author Information

Site: [while-true-do.org](https://while-true-do.org)

Mail: [hello@while-true-do.org](mailto:hello@while-true-do.org)
