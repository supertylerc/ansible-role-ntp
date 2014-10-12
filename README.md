# ntp Ansible Role

This role enables users to install and configure ntp on their hosts.

## Forked!

This repository was forked because it didn't work at all in my
environment.  I've removed many parts of this role, and I've modified
the configuration and variables heavily to conform to internal
standards.  As a result, this repository shares very few similarities to
the upstream repository.  It's almost a new role entirely.  However, the
upstream was the basis, and it was highly inspirational.  For those
reasons, I've chosen to maintain the original list of authors and
provide them credit.

## Requirements

This requires Ansible.  It has been tested with Ansible 1.7, but should
work with Ansible 1.4 and up.

## Examples

1) Install ntp and set the default settings.

```yaml
- hosts: all
  roles:
    - role: ntp
```

2) Install ntp and set some custom servers.

```yaml
- hosts: all
  roles:
    - role: ntp
      ntp.servers:
        - 2.ubuntu.pool.ntp.org
        - 1.ubuntu.pool.ntp.org
```

## License

BSD

## Author Information

- Benno Joy
- René Moser
- Tyler Christiansen
