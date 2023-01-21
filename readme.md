# bviktor.tomcat

## Synopsys

This role installs, configures, and upgrades Tomcat instances.

## Parameters

| Name | Required | Example | Description |
|---|---|---|---|
| `uid` | no | `1234` | UID to run Tomcat under. Defaults to `53`. |
| `gid` | no | `1234` | GID to run Tomcat under. Defaults to `53`. |
| `install_java` | no | `false` | Install Java or not. Defaults to `true`. |
| `tomcat_version` | no | `10.0.27` | Tomcat version to install. This needs to be the specific, full version string. Default value updated occasionally to latest. |
| `tomcat_home` | no | `/opt/apache-tomcat` | Tomcat installation home. Defaults to `/opt/apache-tomcat`. Note that this isn't a directory, this is a symlink, so do not add a trailing slash. |

## Examples

```yml
- include_role:
    name: bviktor.tomcat

- include_role:
    name: bviktor.tomcat
  vars:
    uid: 1234
    gid: 1234
    install_java: false
    tomcat_version: 10.0.27
    tomcat_home: /opt/apache-tomcat
```

## Return Values

N/A

## Support

| Platform | Support | Status |
|---|---|---|
| Linter | ✅ | [![Lint](https://github.com/noobient/ansible-galaxy-tomcat/actions/workflows/lint.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-tomcat/actions/workflows/lint.yml) |
| AlmaLinux 8 | ✅ | [![AlmaLinux 8](https://github.com/noobient/ansible-galaxy-tomcat/actions/workflows/almalinux-8.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-tomcat/actions/workflows/almalinux-8.yml) |
| AlmaLinux 9 | ✅ | [![AlmaLinux 9](https://github.com/noobient/ansible-galaxy-tomcat/actions/workflows/almalinux-9.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-tomcat/actions/workflows/almalinux-9.yml) |
| Fedora 37 | ✅ | [![Fedora 37](https://github.com/noobient/ansible-galaxy-tomcat/actions/workflows/fedora-37.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-tomcat/actions/workflows/fedora-37.yml) |
| Ubuntu 18.04 | ✅ | [![Ubuntu 18.04](https://github.com/noobient/ansible-galaxy-tomcat/actions/workflows/ubuntu-18.04.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-tomcat/actions/workflows/ubuntu-18.04.yml) |
| Ubuntu 20.04 | ✅ | [![Ubuntu 20.04](https://github.com/noobient/ansible-galaxy-tomcat/actions/workflows/ubuntu-20.04.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-tomcat/actions/workflows/ubuntu-20.04.yml) |
| Ubuntu 22.04 | ✅ | [![Ubuntu 22.04](https://github.com/noobient/ansible-galaxy-tomcat/actions/workflows/ubuntu-22.04.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-tomcat/actions/workflows/ubuntu-22.04.yml) |
