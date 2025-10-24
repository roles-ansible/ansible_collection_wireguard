[![Ansible Galaxy](https://ansible.l3d.space/svg/l3d.wireguard.wireguardui_ansible-role.svg)](https://galaxy.ansible.com/ui/repo/published/l3d/wireguard/content/role/wireguardui/)
[![MIT License](https://ansible.l3d.space/svg/l3d.wireguard_license_collection.svg)](LICENSE)
[![Maintainance](https://ansible.l3d.space/svg/l3d.wireguard_maintainance_collection.svg)](https://ansible.l3d.space/#l3d.wireguard)

 ansible role wireguard-ui
=======================

Ansible role to install wireguard-ui

Visit [github.com/ngoduykhanh/wireguard-ui](https://github.com/ngoduykhanh/wireguard-ui) for more information about wireguard-ui.


 Variables
-----------

| Variable                          | Value                             | Description                                                  |
| --------------------------------- | --------------------------------- | ------------------------------------------------------------ |
| ``wireguardui__version``          | ``latest``                        | Wireguard version to install - ``latest`` for newest release |
| ``wireguardui__conf_bind``        | ``127.0.0.1:5000``                | Webserver Bind Port                                          |
| ``wireguardui__conf_int_address`` | ``10.23.42.0/24``                 | Wireguard interface ip addesses *(komma seperated)*          |
| ``wireguardui__conf_int_port``    | ``51820``                         | Wireguard Port                                               |
| ``wireguardui__conf_allowed_ips`` | ``wireguardui__conf_int_address`` | List of allowed wireguard IP addresses                       |
| ``wireguardui__conf_endpoint_ip`` | ``ansible_default_ipv4.address``  | Wireguard endpoint ip                                        |
| ``wireguardui__wg_interface``     | ``wg0``                           | Interface for ip forwarding rule                             |
| ``wireguardui__ipv4_all_forward`` | ``true``                          | set ``net.ipv4.ip_forward``                                  |
| ``wireguardui__ipv4_forward``     | ``false``                         | set ``net.ipv4.conf.wg0.forwarding``                         |
| ``wireguardui__ipv6_all_forward`` | ``true``                          | set ``net.ipv6.conf.all.forwarding``                         |
| ``wireguardui__ipv6_forward``     | ``false``                         | set ``net.ipv6.conf.wg0.forwarding``                         |
| ``wireguardui__ipv6_all``         | ``true``                          | set ``net.ipv6.conf.all.forwarding``                         |
| ``wireguardui__ipv6_no_forward_interfaces`` | ``['default']``         | unset ``net.ipv6.conf.$interface.forwarding``                |
| ``submodules_versioncheck``       | ``false``                         | optional simple version check                                |

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

Contribution
--------------

Please feel free to open an issue or Pull-Request

 Requirements
--------------

Ansible Collections ``community.general`` and ``ansible.posix``
