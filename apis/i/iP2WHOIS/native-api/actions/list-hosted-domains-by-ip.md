# List Hosted Domains by IP with IP2WHOIS

Finds hosted domains in IP2WHOIS by IP address.

## Endpoint

- **Method:** `GET`
- **Path:** `https://domains.ip2whois.com/domains`
- **Base URL:** `https://api.ip2whois.com`
- **Official documentation:** [List Hosted Domains by IP](https://www.ip2location.io/ip2whois-domains-documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | query | `string` | yes | IPv4 or IPv6 address to look up. |
| `page` | query | `number` | no | Page number for hosted domain results. |
