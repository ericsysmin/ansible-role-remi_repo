# THIS REPO IS NO LONGER MAINTAINED - MOVED TO [ericsysmin.system.remi_repo](https://github.com/ericsysmin/ansible-collection-system)

# ericsysmin.remi_repo

[![Build Status](https://travis-ci.org/ericsysmin/ansible-role-repo-remi.svg?branch=master)](https://travis-ci.org/ericsysmin/ansible-role-remi_repo)

[Remi's RPM repository](http://rpms.famillecollet.com/) for RHEL/CentOS.

## Requirements

None.

## Role Variables

| Variable                | Required | Default                                                                                              | Comments                             |
| ----------------------- | -------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------ |
| `remi_repo_url`         | No       | `http://rpms.famillecollet.com/enterprise/remi-release-{{ ansible_distribution_major_version }}.rpm` | Set url for remi repository          |
| `remi_repo_gpg_key_url` | No       | `http://rpms.remirepo.net/RPM-GPG-KEY-remi`                                                          | GPG key location for remi repository |
| `remi_repo_enable_list` | No       | `[]`                                                                                                 | List of repositories to enable       |

## Dependencies

None.

## Example Playbook

```yaml
- hosts: servers
  roles:
    - ericsysmin.repo-remi
      remi_repo_enable_list:
        - remi-php72
```

## License

MIT

## Author Information

[ericsysmin](https://ericsysmin.com/)
