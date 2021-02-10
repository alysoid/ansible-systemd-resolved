# [Catena](https://github.com/alysoid/catena) - Resolve Ansible Role

Manage system DNS resolver via systemd using [systemd-resolved](https://man.archlinux.org/man/systemd-resolved.8.en), a system service that provides network name resolution to local applications. It implements a caching and validating DNS/DNSSEC stub resolver, as well as an LLMNR and MulticastDNS resolver and responder.

## Role default variables

| Variable           | Default | Info
| ------------------ | ------- | ------------------
| `systemd_resolved` | `{}`    | Set configuration files that control local DNS and LLMNR name resolution.
| `resolve_cleanup`  | `no`    | Remove existing configuration files: `/etc/systemd/resolved.conf.d/*.conf`.

### `systemd_resolved`

Manage [resolved.conf.d - Network Name Resolution configuration files](https://man.archlinux.org/man/resolved.conf.5.en).

Configuration files will have the .conf extension and will be placed in the configuration snippets directory `/etc/systemd/network`.
