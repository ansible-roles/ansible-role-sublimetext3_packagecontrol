# ansible-role-sublimetext3_packagecontrol
[![Build Status](https://travis-ci.org/cmprescott/ansible-role-sublimetext3_packagecontrol.svg?branch=feature/IntegrationTest)](https://travis-ci.org/cmprescott/ansible-role-sublimetext3_packagecontrol)

Ansible role to install Sublime Text 3 [Package Control](https://packagecontrol.io/) and configure packages list.

## Prerequisites

You must [install sublimetext3](https://galaxy.ansible.com/list#/roles/3070) before.

## Example Playbook

```yml

  vars:
    # --- Defaults (Welcome to override!) ---
    packagecontrol_url: "https://packagecontrol.io/Package Control.sublime-package"
    packagecontrol_dir_bin: "~/.config/sublime-text-3/Installed Packages"
    packagecontrol_dir_cfg: "~/.config/sublime-text-3/Packages/User"    
    packagecontrol_owner: "{{ ansible_ssh_user }}"
    packagecontrol_group: "{{ ansible_ssh_user }}"
    packagecontrol_backup: yes
    # --- Settings (Need to override!) ---
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
