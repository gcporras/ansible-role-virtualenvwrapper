ansible-role-virtualenvwrapper
========

An [Ansible](http://www.ansible.com/home) Role that installs and configures
[virtualenvwrapper](http://virtualenvwrapper.readthedocs.org).

[![Build Status](https://travis-ci.org/gcporras/ansible-role-virtualenvwrapper.png?branch=master)](https://travis-ci.org/gcporras/ansible-role-virtualenvwrapper)

Requirements
------------

The following tools are required:
- [pip](https://pip.pypa.io/en/latest/installing.html) a tool for installing and managing Python packages.

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

`virtualenvwrapper_version` per default set to `4.3.1`

The version of virtualenvwrapper that will be installed.

`virtualenvwrapper_shell_rc_file` per default set to
`{{ ansible_env['HOME'] }}/.{{ ansible_env['SHELL'] | replace('/bin/','') }}rc`

The shell's configuration file for which virtualenvwrapper variables will be set.

`virtualenvwrapper_venvs_home` per default set to `{{ ansible_env['HOME'] }}/.virtualenvs`

The path to place your virtual environements (sets WORKON_HOME env variable).

Dependencies
------------

None.

Example Playbook
-------------------------

    - hosts: servers
      roles:
         - role: "gcporras.virtualenvwrapper"
           sudo: yes
           tags:
            - virtualenvwrapper
License
-------

MIT

## Author Information

This role was created in 2014 by Gerardo Cepeda Porras.
