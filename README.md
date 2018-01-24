#Ansible Role: MacOS
[![Build Status][travis-badge]][travis-link]
[![MIT licensed][mit-badge]][mit-link]
[![Galaxy Role][role-badge]][galaxy-link]

Configures MacOS by mostly using the defaults module

Requirements
------------

homebrew

Role Variables
--------------

See defaults/main.yml

Dependencies
------------

none

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: KingLoui.macos }

[galaxy-link]: https://galaxy.ansible.com/KingLoui/macos/
[mit-badge]: https://img.shields.io/badge/license-MIT-blue.svg
[mit-link]: https://raw.githubusercontent.com/kingloui/ansible-role-macos/master/LICENSE
[role-badge]: https://img.shields.io/badge/role-KingLoui.macos-blue.svg
[travis-badge]: https://travis-ci.org/KingLoui/ansible-role-macos.svg?branch=master
[travis-link]: https://travis-ci.org/KingLoui/ansible-role-macos