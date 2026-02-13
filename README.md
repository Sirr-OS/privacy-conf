# privacy-conf

This package provides default privacy and DNS hardening configurations for Sirr OS.

## Installed Files

- `/etc/dnscrypt-proxy/dnscrypt-proxy.toml` – configuration for dnscrypt-proxy
- `/etc/NetworkManager/conf.d/10-dnscrypt.conf` – forces NetworkManager to ignore automatic DNS
- `/etc/resolv.conf` – default DNS set to localhost (127.0.0.1)

## Purpose

- Force all DNS traffic through dnscrypt-proxy.
- Prevent accidental DNS leaks via DHCP or external network connections.
- Integrate privacy-focused defaults for NetworkManager.

## Installation

```bash
sudo dpkg -i privacy-conf_1.0.0_all.deb
```

## Post-Installation

- NetworkManager will restart automatically to apply the configuration.
- All DNS queries will use 127.0.0.1 (dnscrypt-proxy).
- Optional: Add firewall rules to block any outgoing DNS requests not going through localhost.

---

## Author

Commander.Z3R0

---
