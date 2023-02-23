![Ansible Lint](https://github.com/johanneskastl/ansible-role-opensuse_leap_micro_add_regular_repositories/workflows/Ansible%20Lint/badge.svg)

opensuse_leap_micro_add_regular_repositories
=========

Add the regular openSUSE Leap repositories on a openSUSE Leap Micro installation.

Requirements
------------

None.

Role Variables
--------------

By default, this role adds all of the repos that are present on a fresh openSUSE Leap 15.4 installation in the same state (enabled, disabled) they are on Leap 15.4. The only exceptions are the `repo-source.repo` and the `repo-debug.repo`, to not interfere with the ones from Leap Micro.

In case you want to enable or disable repos, each one has a `..._enabled` variable that can be set to '1' (enabled) or '0' (disabled).

- `repo_oss_enabled`: OSS repository (Default value: `'1'`)
- `repo_non_oss_enabled`: Non-OSS repository (Default value: `'1'`)
- `repo_update_oss_enabled`: Updates for the OSS repository (Default value: `'1'`)
- `repo_update_non_oss_enabled`: Updates for the Non-OSS repository(Default value: `'1'`)
- `repo_backports_update_enabled`: Updates for the Backports repository (Default value: `'1'`)
- `repo_sle_update_enabled`: Updates for the SLE repository (Default value: `'1'`)
- `repo_debug_non_oss_enabled`: Debug repository (Non-OSS) (Default value: `'0'`)
- `repo_debug_update_enabled`: Updates for the Debug repository (OSS) (Default value: `'0'`)
- `repo_debug_update_non_oss_enabled`: Updates for the Debug repository (Non-OSS) (Default value: `'0'`)
- `repo_backports_debug_update_enabled`: Updates for the Backports Debug repository (Default value: `'0'`)
- `repo_sle_debug_update_enabled`: Updates for the Debug SLE repository (Default value: `'0'`)


Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: 'johanneskastl.opensuse_leap_micro_add_regular_repositories'

License
-------

BSD-3-Clause

Author Information
------------------

I am Johannes Kastl, reachable via kastl@b1-systems.de.
