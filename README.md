# ansible-role-podman

[![GitHub latest release](https://img.shields.io/github/v/release/dmotte/ansible-role-podman?logo=github&style=flat-square)](https://github.com/dmotte/ansible-role-podman/actions)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-dmotte.podman-blueviolet?logo=ansible&style=flat-square)](https://galaxy.ansible.com/dmotte/podman)

Ansible role to install **Podman** on Debian hosts.

This role has been tested with **Debian 11** (_bullseye_).

_Podman_ will be installed using the official `podman` package from the _Debian_ repositories. In addition, this role allows you to configure some other related stuff, such as the **Podman socket** and the `podman-auto-update` service, both for the **system scope** and for **individual users**.

## Usage

1. Install this role using the `ansible-galaxy` CLI tool
2. You can then include it into the `tasks` section of your _Ansible Playbook_. See [`test/playbook.yml`](test/playbook.yml) for an example of how to do that. Remember to replace the role name with `dmotte.podman`.

> **Note**: this role must be run as root (`ansible_become: true`).

### Role variables

See [`defaults/main.yml`](defaults/main.yml).

## Development

If you want to contribute to this project, you can use the [`test/playbook.yml`](test/playbook.yml) file to test the role while editing it.

Place your inventory file (e.g. `hosts.yml`) inside the `test` folder.

Edit the `vars` section of the [`test/playbook.yml`](test/playbook.yml) file to match your scenario.

You can then **execute the playbook** against your host:

```bash
cd test/
ansible-playbook -i hosts.yml playbook.yml
```
