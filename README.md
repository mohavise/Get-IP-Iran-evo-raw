# Iran IP Address Lists — IPv4 and IPv6 CIDR

[![Sync Raw IP Lists](https://github.com/mohavise/Get-IP-Iran-evo-raw/actions/workflows/sync-raw-lists.yml/badge.svg)](https://github.com/mohavise/Get-IP-Iran-evo-raw/actions/workflows/sync-raw-lists.yml)
[![IPv4](https://img.shields.io/badge/list-IPv4-blue)](https://raw.githubusercontent.com/mohavise/Get-IP-Iran-evo-raw/main/iran-ipv4.txt)
[![IPv6](https://img.shields.io/badge/list-IPv6-blueviolet)](https://raw.githubusercontent.com/mohavise/Get-IP-Iran-evo-raw/main/iran-ipv6.txt)

Automatically updated **Iranian IPv4 and IPv6 CIDR lists** in a clean, raw, and machine-readable format.

This repository extracts Iran IP address ranges from the master [`Get-IP-Iran-evo`](https://github.com/mohavise/Get-IP-Iran-evo) project and publishes IPv4 and IPv6 prefixes as separate plain-text files. Each line contains one CIDR network with no MikroTik commands, comments, or additional formatting.

## Raw Iran IP Lists

| IP version | File | Direct raw URL |
|---|---|---|
| IPv4 | [`iran-ipv4.txt`](./iran-ipv4.txt) | [Download raw IPv4 list](https://raw.githubusercontent.com/mohavise/Get-IP-Iran-evo-raw/main/iran-ipv4.txt) |
| IPv6 | [`iran-ipv6.txt`](./iran-ipv6.txt) | [Download raw IPv6 list](https://raw.githubusercontent.com/mohavise/Get-IP-Iran-evo-raw/main/iran-ipv6.txt) |

### Direct URLs

```text
https://raw.githubusercontent.com/mohavise/Get-IP-Iran-evo-raw/main/iran-ipv4.txt
https://raw.githubusercontent.com/mohavise/Get-IP-Iran-evo-raw/main/iran-ipv6.txt
```

## Features

- Separate Iran IPv4 and IPv6 CIDR lists
- One network prefix per line
- Plain-text and machine-readable output
- Automatically synchronized from the master repository
- Duplicate entries removed
- Validation prevents empty or incomplete lists from replacing valid data
- Suitable for routers, firewalls, Linux systems, proxies, VPN gateways, DNS platforms, and automation scripts

## File Format

### IPv4 example

```text
5.22.0.0/17
31.2.128.0/17
37.32.0.0/19
```

### IPv6 example

```text
2001:678:b0::/46
2001:df0:66c0::/48
2a00:1e48::/32
```

## Usage Examples

### Download with curl

```bash
curl -fsSL -o iran-ipv4.txt \
  https://raw.githubusercontent.com/mohavise/Get-IP-Iran-evo-raw/main/iran-ipv4.txt

curl -fsSL -o iran-ipv6.txt \
  https://raw.githubusercontent.com/mohavise/Get-IP-Iran-evo-raw/main/iran-ipv6.txt
```

### Download with wget

```bash
wget -O iran-ipv4.txt \
  https://raw.githubusercontent.com/mohavise/Get-IP-Iran-evo-raw/main/iran-ipv4.txt

wget -O iran-ipv6.txt \
  https://raw.githubusercontent.com/mohavise/Get-IP-Iran-evo-raw/main/iran-ipv6.txt
```

### Read the lists in a shell script

```bash
while IFS= read -r subnet; do
  printf 'IPv4 subnet: %s\n' "$subnet"
done < iran-ipv4.txt
```

## Common Use Cases

These Iran IP range lists can be used for:

- Geo-based firewall rules
- Routing and policy-routing automation
- VPN and proxy bypass lists
- Iran traffic identification
- Network monitoring and reporting
- Security filtering and access-control systems
- MikroTik, Linux, FortiGate, pfSense, OPNsense, and other network platforms

> This repository provides raw CIDR data only. Platform-specific firewall or router commands should be generated separately according to your environment.

## Automatic Updates

A GitHub Actions workflow periodically:

1. Downloads the latest IPv4 and IPv6 source files from the master repository.
2. Extracts valid CIDR prefixes.
3. Separates IPv4 and IPv6 networks.
4. Sorts and removes duplicate entries.
5. Validates the generated files.
6. Commits changes only when the IP lists have changed.

Source project:

- [`mohavise/Get-IP-Iran-evo`](https://github.com/mohavise/Get-IP-Iran-evo)

## Data Accuracy

IP address allocations can change over time. The lists are automatically refreshed from the upstream project, but no IP geolocation dataset can guarantee permanent or real-time accuracy for every network.

Before using these lists in production, test the resulting firewall, routing, proxy, or access-control behaviour in your own environment.

## Contributing

Issues and pull requests are welcome for:

- Invalid or missing prefixes
- Automation improvements
- Validation enhancements
- Documentation corrections

For issues related to the original IP collection process, report them in the master [`Get-IP-Iran-evo`](https://github.com/mohavise/Get-IP-Iran-evo) repository.

## Keywords

Iran IP list, Iranian IP ranges, Iran IPv4 CIDR, Iran IPv6 CIDR, Iran subnet list, Iran IP database, Iran network prefixes, raw IP list, firewall address list, geo IP filtering, MikroTik Iran IP, Linux IP set, VPN bypass list.

## License

This repository republishes processed data from the master project. Review the source repository and applicable data-source terms before redistribution or commercial use.
