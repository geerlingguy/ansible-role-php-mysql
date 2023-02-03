# Ansible Role: PHP-MySQL

[![CI](https://github.com/geerlingguy/ansible-role-php-mysql/workflows/CI/badge.svg?event=push)](https://github.com/geerlingguy/ansible-role-php-mysql/actions?query=workflow%3ACI)

Installs PHP [MySQL](https://www.mysql.com/) support on Linux.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    php_enablerepo: ""

(RedHat/CentOS only) If you have enabled any additional repositories (might I suggest geerlingguy.repo-epel or geerlingguy.repo-remi), those repositories can be listed under this variable (e.g. `remi,epel`). This can allow you to install later versions of PHP packages.

    php_mysql_package: php-mysqlnd # RedHat
    php_mysql_package: php8.2-mysql # Debian

The PHP MySQL package to install via apt/yum. This should only be overridden if you need to install a unique/special package for MySQL support, as in the case of using software collections on Enterprise Linux, or if you need to set an old package name (e.g. `php-mysql` on RHEL 7).

## Dependencies

  - geerlingguy.php

## Example Playbook

    - hosts: webservers
      roles:
        - { role: geerlingguy.php-mysql }

## License

MIT / BSD

## Author Information

This role was created in 2014 by [Jeff Geerling](https://www.jeffgeerling.com/), author of [Ansible for DevOps](https://www.ansiblefordevops.com/).
