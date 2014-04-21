# Ansible Role: PHP-MySQL

Installs PHP MySQL support on RedHat Enterprise Linux or CentOS 6.x servers.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `vars/main.yml`):

    php_enablerepo: ""

If you have enabled any additional repositories (might I suggest geerlingguy.repo-epel or geerlingguy.repo-remi), those repositories can be listed under this variable (e.g. `remi,epel`). This can be handy, as an example, if you want to install the latest version of PHP 5.4, which is in the Remi repository.

## Dependencies

  - geerlingguy.php
  - geerlingguy.mysql

## Example Playbook

    - hosts: webservers
      roles:
        - { role: geerlingguy.php-mysql }

## License

MIT / BSD

## Author Information

This role was created in 2014 by [Jeff Geerling](http://jeffgeerling.com/), author of [Ansible for DevOps](http://ansiblefordevops.com/).
