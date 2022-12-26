Ansible Davinci LineageOS
=========

Build Davinci LineageOS on Debian 11.

Requirements
------------

This role requires a Git configured on the remote server.
For instance you can invoke the role in your playbook like:
```yaml
- hosts: aws
  roles:
    - role: davinci
      become: yes
      vars:
        git_user_email: you@example.com
        git_user_name: Your Name
```

Role Variables
--------------

Available variables are listed in `defaults/main.yml`:

```yaml
git_user_email: you@example.com
git_user_name: Your Name
```
The Git user configuration.

```yaml
build_dir: /tmp/android
```
The directory that will be used in order to build LineageOS

```yaml
skip_sync: no
```
Download the source code every time. Set it to `yes`
if you have already downloaded the source code.

Dependencies
------------

There is no dependencies for this role.

Example Playbook
----------------

```yaml
- hosts: localhost
  become: yes
  roles:
    - role: davinci
```

License
-------

BSD

Author Information
------------------

Role created by Flowrey
