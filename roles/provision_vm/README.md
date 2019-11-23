# provision_vm

## Table Of Contents

* [About](#about)
* [Role Defaults](#role-defaults)
* [License](#license)
* [Author](#author)

## About

> your description

[Back to table of contents](#table-of-contents)

## Role Defaults

**Quicklist**: [management_pass](#management_pass),
[management_public_key](#management_public_key),
[management_user](#management_user)

### management_pass 

* *help*: TODO.

[Back to table of contents](#table-of-contents)

### management_public_key 

* *help*: TODO.

[Back to table of contents](#table-of-contents)

### management_user 

* *help*: TODO.

[Back to table of contents](#table-of-contents)

## Example Playbooks

### Basic Usage

```yaml
- name: Provision new host(s)
  hosts: control
  remote_user: "{{ provision_user }}"
  become: true
  become_user: root
  vars: # These variables are needed to connect to the new virtual machine(s)
    ansible_become_pass: "{{ provision_pass }}"
    ansible_ssh_pass: "{{ provision_pass }}"
  roles:
  - role: provision_vm
    management_user_name: "{{ mgmt_user }}"
    management_user_password: "{{ mgmt_pass }}"
    management_public_key: "{{ mgmt_key }}"
```


[Back to table of contents](#table-of-contents)


## License

license (GPLv2, CC-BY, etc)

[Back to table of contents](#table-of-contents)

## Author

your name

[Back to table of contents](#table-of-contents)
