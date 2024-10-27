[![Ansible Galaxy](https://ansible.l3d.space/svg/l3d.wireguard.wireguardui_ansible-role.svg)](https://galaxy.ansible.com/ui/repo/published/l3d/wireguard/content/role/wireguardui/)
[![MIT License](https://ansible.l3d.space/svg/l3d.wireguard_license_collection.svg)](LICENSE)
[![Maintainance](https://ansible.l3d.space/svg/l3d.wireguard_maintainance_collection.svg)](https://ansible.l3d.space/#l3d.wireguard)

 ansible role wireguard-ui
=======================

Ansible role to install wireguard-ui

Visit [github.com/ngoduykhanh/wireguard-ui](https://github.com/ngoduykhanh/wireguard-ui) for more information about wireguard-ui.


 Variables
-----------

| Variable                      | Value      | Description                                                  |
| ----------------------------- | ---------- | ------------------------------------------------------------ |
| ``wireguardui__version``      | ``latest`` | Wireguard version to install - ``latest`` for newest release |
| ``wireguardui__wg_interface`` | ``wg0``    | Interface for ip forwarding rule                             |
| ``wireguardui__ipv4_forward`` | ``true``   | set ``net.ipv4.conf.wg0.forwarding``                         |
| ``wireguardui__ipv6_forward`` | ``true``   | set ``net.ipv6.conf.wg0.forwarding``                         |
| ``submodules_versioncheck``   | ``false``  | optional simple version check                                |

 Contribution
--------------

Please feel free to open an issue or Pull-Request

 Requirements
--------------

Collection ``community.general``
