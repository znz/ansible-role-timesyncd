# Ansible role for `systemd-timesyncd`

- Setup `/etc/systemd/timesyncd.conf`
- Run `timedatectl set-ntp true`

## Requirements

- Debian
- Ubuntu

## Role Variables

### Common

- `timesyncd_ntp_servers`: NTP servers

## Dependencies

None.

## Example Playbook

Normal usage:

    ---
    - hosts: all
      become: yes
      roles:
      - znz.timesyncd

With NTP servers:

    ---
    - hosts: all
      become: yes
      roles:
      - { role: znz.timesyncd, timesyncd_ntp_servers: ['ntp.nict.jp', 'ntp.mfeed.ad.jp'] }

## License

MIT License
