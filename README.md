[![collection l3d.wireguard](https://ansible.l3d.space/svg/l3d.wireguard_ansible-collection_collection.svg)](https://galaxy.ansible.com/ui/repo/published/l3d/wireguard/)
[![Maintainance](https://ansible.l3d.space/svg/l3d.wireguard_maintainance_collection.svg)](https://ansible.l3d.space/#l3d.wireguard)
[![License](https://ansible.l3d.space/svg/l3d.wireguard_license_collection.svg)](LICENSE)

 Ansible Collection - l3d.wireguard
============================

This is the Ansible Collection ``l3d.wireguard``. A collection to to install wireguard-ui on linux servers.

## Ansible Roles in l3d.wireguard
- [![l3d.wireguard.wireguardui](https://ansible.l3d.space/svg/l3d.wireguard.wireguardui_ansible-role.svg)](https://galaxy.ansible.com/ui/repo/published/l3d/wireguard/content/role/wireguardui/) - Ansible role to install wireguard-ui

## Using this Collection
You can install the collection using ansible-galaxy by running:
```bash
ansible-galaxy collection install l3d.wireguard:1.0.2
```

Remember you can to Upgrade to the latest version of the l3d.wireguard collection using the ``--upgrade`` parameter:
```bash
ansible-galaxy collection install l3d.wireguard --upgrade
```


Or you could clone this collection in your local ansible project for example to ``collections/ansible_collections/l3d.wireguard/``. Make sure you checkout [git submodules](https://git-scm.com/docs/git-submodule) too. Example:
```
# Clone git Repo with submodules to specified path
git clone --recursive https://github.com/roles-ansible/ansible_collection_wireguard.git collections/ansible_collections/l3d/wireguard/

# change directory
cd collections/ansible_collections/l3d.wireguard/

# optionally init git submodules
git submodule update --init --recursive

# optionally install all requirements
ansible-galaxy collection install -r requirements.yml --upgrade
```

You can also list a collection in ``requirements.yml``:
```yaml
---
collections:
  - name: l3d.wireguard
    version: ">=1.0.2"
```

## Example Playbook
Example Playbook using the l3d.wireguard.wireguardui role:

```yaml
---
- name: "Install and Setup Wireguard-UI"
  hosts: wireguard.example.com
  roles:
    - {role: l3d.wireguard.wireguardui, tags: wireguardui}
  vars:
    wireguardui__conf_int_address: ['10.42.42.0/24', 'fd42:1337:4223::/48']
```

## Requirements
The roles in this collection using the ``community.general`` and ``ansible.posix`` ansible Collections.
