# Ansible Role: el_repo_version

Pin CentOS to a specific minor release hosted on the CentOS Vault.

## Requirements

- Ansible >= 2.9

## Role Variables

- el_repo_version (string) = The exact version of CentOS to pin the repositories to. Only older versions hosted on [vault.centos.org](http://vault.centos.org/) are supported.
    - CentOS 7:
        - 7.0.1406
        - 7.1.1503
        - 7.2.1511
        - 7.3.1611
        - 7.4.1708
        - 7.5.1804
        - 7.6.1810
        - 7.7.1908
    - CentOS 8:
        - 8.0.1905
        - 8.1.1911

## Dependencies

None.

## Example Playbook

```
---
- hosts: centos7
  roles:
    - name: el_repo_version
      vars:
        el_repo_version: C7.7.1908
```

## License

Apache v2.0
