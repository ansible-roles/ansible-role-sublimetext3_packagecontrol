# ansible-role-sublimetext3_packagecontrol

Ansible role to install Sublime Text 3 [Package Control](https://packagecontrol.io/) and configure packages list.

## Prerequisites

You must [install sublimetext3](https://galaxy.ansible.com/list#/roles/3070) before.

## Example Playbook

```yml

  vars:
    packagecontrol_owner: some-user
    packagecontrol_group: www-data

    packagecontrol_packages:
     - "AutoFileName"
     - "GitGutter"
     - "Symfony2 Snippets"
     - "Twig"
     - "Terminal"

  roles:
    - { role: igor_mukhin.sublimetext3_packagecontrol, tags: sublimetext3 }

```

## License

MIT
