# Ansible Role: macOS

[![Build Status][travis-badge]][travis-link]
[![MIT licensed][mit-badge]][mit-link]
[![Galaxy Role][role-badge]][galaxy-link]

Configures macOS and default apple applications by mostly using the defaults module.

## Requirements

- **Homebrew**: Requires homebrew already installed (you can use geerlingguy.homebrew to install it on your Mac).

## Role Variables

Most vars are self explanatory just check out defaults at defaults/main.yml



##### default applications
You can set default filetype associations like this:

	system_default_applications:
	  - { extension: avi, handler: com.colliderli.iina }
	  - { extension: md, handler: com.uranusjr.macdown }
	  - { extension: cfg, handler: com.sublimetext.3 }

##### dock apps

	dock_apps:
	  - name: Safari
	    path: /Applications/Safari.app
	  - name: iTunes
	    path: /Applications/iTunes.app
	  - name: Mail
	    path: /Applications/Mail.app   
	  - name: iTerm
	    path: /Applications/iTerm.app
	  - name: Tower
	    path: /Applications/Tower.app
	  - name: Sublime Text
	    path: /Applications/Sublime Text.app
	dock_spacers:
	  - after: iTunes
	  - after: Mail


## Dependencies

- (Soft dependency) geerlingguy.homebrew

## Example Playbook

    - hosts: servers
      roles:
         - geerlingguy.homebrew
         - kinglouie.macos



[galaxy-link]: https://galaxy.ansible.com/kinglouie/macos/
[mit-badge]: https://img.shields.io/badge/license-MIT-blue.svg
[mit-link]: https://raw.githubusercontent.com/kinglouie/ansible-role-macos/master/LICENSE
[role-badge]: https://img.shields.io/badge/role-kinglouie.macos-blue.svg
[travis-badge]: https://travis-ci.org/kinglouie/ansible-role-macos.svg?branch=master
[travis-link]: https://travis-ci.org/kinglouie/ansible-role-macos