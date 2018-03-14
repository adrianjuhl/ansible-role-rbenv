Ansible role: rbenv
=========

Installs [rbenv](https://github.com/sstephenson/rbenv).

Requirements
------------

None.

Role Variables
--------------
Available variables are listed below, along with default values (see `defaults/main.yml`):

    rbenv_repo: "https://github.com/rbenv/rbenv.git"

The repository that rbenv is to be cloned from.

    rbenv_plugins: 
      - { name: "ruby-build", repo: "https://github.com/rbenv/ruby-build.git", version: "master" }

The rbenv plugins that are also to be installed.
 
    rbenv_root: "~/.rbenv"

The location that rbenv is to be installed to.

    rbenv_user: "{{ ansible_user }}"

The user account that rbenv is to be installed for.

Dependencies
------------

  - [adrianjuhl.git](https://galaxy.ansible.com/adrianjuhl/git/)

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: adrianjuhl.rbenv }

License
-------

MIT

Author Information
------------------

[Adrian Juhl](http://github.com/adrianjuhl)
