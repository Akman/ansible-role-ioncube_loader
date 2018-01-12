# Ansible Role: ioncube-loader

Installs Ioncube-loader on Linux.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values:

    workspace: /root
    
    php_version: '7.1'
    php_ioncube_loader_module_path: "/usr/lib/php5/modules"
    php_ioncube_loader_module_filename: "ioncube_loader_lin_{{ php_version }}.so"
    php_ioncube_loader_config_filename: "10-ioncube.ini"
    php_extension_conf_paths:
      - "/etc/php/{{ php_version }}/fpm/conf.d"
      - "/etc/php/{{ php_version }}/apache2/conf.d"
      - "/etc/php/{{ php_version }}/cli/conf.d"

## Dependencies

None.

## Example Playbook

    - hosts: all
      roles:
        - akman.ioncube-loader

*Inside `vars/main.yml`*:

    workspace: /root
    php_version: '7.2'

## License

MIT / BSD

## Author Information

This role was created in 2017 by Alexander Kapitman
