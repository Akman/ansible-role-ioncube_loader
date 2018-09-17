# Ansible Role: ioncube_loader

Installs Ioncube loader on Linux.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values:

    workspace: /root
    php_ioncube_user: root
    php_ioncube_group: root
    
    php_version: '7.2'

    php_ioncube_loader_module_path: "/usr/lib/php/{{ php_version }}/modules"
    php_ioncube_loader_module_filename: "ioncube_loader_lin_{{ php_version }}.so"

    php_ioncube_loader_config_filename: "10-ioncube.ini"

    php_extension_conf_paths:
      - "/etc/php/{{ php_version }}/fpm/conf.d"
      - "/etc/php/{{ php_version }}/apache2/conf.d"
      - "/etc/php/{{ php_version }}/cli/conf.d"

## Dependencies

  - geerlingguy.php

## Example Playbook

    - hosts: all
      roles:
        - akman.ioncube_loader

*Inside `vars/main.yml`*:

    php_version: '7.2'

## License

MIT / BSD

## Author Information

This role was created in 2017 by Alexander Kapitman
