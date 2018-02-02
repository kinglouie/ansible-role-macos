# Ansible Role: macOS

[![Build Status][travis-badge]][travis-link]
[![MIT licensed][mit-badge]][mit-link]
[![Galaxy Role][role-badge]][galaxy-link]

Configures macOS and default apple applications by mostly using the defaults module.

## Requirements

- **Homebrew**: Requires homebrew already installed (you can use geerlingguy.homebrew to install it on your Mac).

## Role Variables

There are quite a few, check out [defaults/main.yml](defaults/main.yml), most vars should be self explanatory.

#### Override defaults:
Since this role's vars are organized in dictionaries you have to override the defaults in an own dictionary that will be merged with the defaults.

In order to override this:

```
system_defaults:
  ui:
    interface_style: "Light"
```
You have to ommit the `_defaults` suffix like this:

```
system:
  ui:
    interface_style: "Dark"
```

## Dependencies

- (Soft dependency) geerlingguy.homebrew

## Example Playbook

    - hosts: all
      roles:
         - geerlingguy.homebrew
         - kinglouie.macos

## TODO

- Adjust defaults so they match macOS defaults.

## Contributing

I will happily merge PR's with new tasks, just make sure...

- that your tasks are idempotent
- that the defaults match the defaults of macOS



[galaxy-link]: https://galaxy.ansible.com/kinglouie/macos/
[mit-badge]: https://img.shields.io/badge/license-MIT-blue.svg
[mit-link]: https://raw.githubusercontent.com/kinglouie/ansible-role-macos/master/LICENSE
[role-badge]: https://img.shields.io/badge/role-kinglouie.macos-blue.svg
[travis-badge]: https://travis-ci.org/kinglouie/ansible-role-macos.svg?branch=master
[travis-link]: https://travis-ci.org/kinglouie/ansible-role-macos