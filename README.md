Ansible Role: Common Tasks
=========

Ansible role to install common tasks on RHEL/CentOS
This role installs the following applications/services
- screen 
- telnet 
- deltarpm 
- dos2unix 
- vim 
- zip 
- unzip 
- bzip2 
- gzip 
- patch 
- wget

Requirements
------------
role_user & role_group must be defined in a .yml file in either group_vars/ or host_vars/

Role Variables
--------------

project_dirs: (Optional) defines a list of dictionaries with key.value pairs for directory path, and permissions.

```aidl
project_dirs:
  - path: /path/to/first_directory
    perm: "0777"

 - path: /path/to/second_directory
   perm: "0755"
```

role_user: (string) Owner name for files and folders
role_group: (string) Group name for files and folders

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: cyberitas.ansible_role_common }

License
-------

MIT

Author Information
------------------

Created in 2019 by James Dugger for Cyberitas Technologies, LLC
