# Ansible Role - Vagrant
[![Build Status](https://travis-ci.org/brentwg/ansible-role-vagrant.svg?branch=master)](https://travis-ci.org/brentwg/ansible-role-vagrant)

This role installs Hashicorp's [Vagrant](https://www.vagrantup.com) application.

## Requirements 

None.

## Role Variables 

User modifiable variables and defaults are listed below. (For all variables, see defaults/main.yml):
```
vagrant_version: 2.0.2
```
The version of Vagrant to install.

```
vagrant_arch: x86_64
```
The system architecture that you are using (eg. 386 or amd64).

## Dependencies

Traditionally, Vagrant is usually installed along with [VirtualBox](https://www.virtualbox.org/). However, I use [libvirt](https://libvirt.org/), so I don't bother.

## Sample Playbook
```
- hosts: all

  vars:
    vagrant_version: "1.2.0"
    vagrant_arch: "amd64"
  
  roles:
    - brentwg.vagrant
```
