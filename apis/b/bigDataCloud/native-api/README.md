# BigDataCloud: Native API Reference

A consolidated summary of BigDataCloud's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://www.bigdatacloud.com/support/getting-started
- **API base URL:** `https://api-bdc.net`

## Authentication

### API Key

Connect BigDataCloud with an API key from your account dashboard.

### Credentials

- **API Key:** `apiKey` · required · Your BigDataCloud API key from the account dashboard.

[Official authentication documentation](https://www.bigdatacloud.com/support/javascript-api-client)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get ASN Info](actions/get-asn-info.md) | `GET /data/asn-info` | [docs](https://www.bigdatacloud.com/ip-geolocation/asn-short-info-api) |
| [Get ASN Info Extended](actions/get-asn-info-extended.md) | `GET /data/asn-info-full` | [docs](https://www.bigdatacloud.com/network-engineering/asn-info-extended-api) |
| [Get ASN Receiving From](actions/get-asn-receiving-from.md) | `GET /data/asn-info-receiving-from` | [docs](https://www.bigdatacloud.com/network-engineering/asn-info-receiving-from) |
| [Get ASN Transit To](actions/get-asn-transit-to.md) | `GET /data/asn-info-transit-to` | [docs](https://www.bigdatacloud.com/network-engineering/asn-info-transit-to) |
| [Get Country by IP](actions/get-country-by-ip.md) | `GET /data/country-by-ip` | [docs](https://www.bigdatacloud.com/ip-geolocation/country-by-ip-address-api) |
| [Get Country Info](actions/get-country-info.md) | `GET /data/country-info` | [docs](https://www.bigdatacloud.com/ip-geolocation/country-info-api) |
| [Get Hazard Report](actions/get-hazard-report.md) | `GET /data/hazard-report` | [docs](https://www.bigdatacloud.com/ip-geolocation/hazard-report-api) |
| [Get IP Geolocation Report](actions/get-ip-geolocation.md) | `GET /data/ip-geolocation-full` | [docs](https://www.bigdatacloud.com/ip-geolocation/ip-address-geolocation-with-confidence-area-and-hazard-report-api) |
| [Get IP Geolocation](actions/get-ip-geolocation-basic.md) | `GET /data/ip-geolocation` | [docs](https://www.bigdatacloud.com/ip-geolocation/ip-address-geolocation-api) |
| [Get IP Geolocation with Confidence Area](actions/get-ip-geolocation-with-confidence-area.md) | `GET /data/ip-geolocation-with-confidence` | [docs](https://www.bigdatacloud.com/ip-geolocation/ip-address-geolocation-with-confidence-area-api) |
| [Get IPv4 Address Space Monitoring](actions/get-ipv4-address-space-monitoring.md) | `GET /data/address-space-stats-ipv4` | [docs](https://www.bigdatacloud.com/network-engineering/ipv4-address-space-monitoring-api) |
| [Get Network by IP](actions/get-network-by-ip.md) | `GET /data/network-by-ip` | [docs](https://www.bigdatacloud.com/ip-geolocation/network-by-ip-address-api) |
| [Get Time Zone by IP](actions/get-time-zone-by-ip.md) | `GET /data/timezone-by-ip` | [docs](https://www.bigdatacloud.com/ip-geolocation/timezone-by-ip-address-api) |
| [Get Time Zone by Location](actions/get-time-zone-by-location.md) | `GET /data/timezone-by-location` | [docs](https://www.bigdatacloud.com/reverse-geocoding/timezone-by-location-api) |
| [Get Time Zone Info](actions/get-time-zone-info.md) | `GET /data/timezone-info` | [docs](https://www.bigdatacloud.com/ip-geolocation/timezone-info-api) |
| [Get User Risk](actions/get-user-risk.md) | `GET /data/user-risk` | [docs](https://www.bigdatacloud.com/ip-geolocation/user-risk-api) |
| [List ASN Ranks](actions/list-asn-ranks.md) | `GET /data/asn-rank-list` | [docs](https://www.bigdatacloud.com/network-engineering/asn-rank-list) |
| [List BGP Active Prefixes](actions/list-bgp-active-prefixes.md) | `GET /data/prefixes-list` | [docs](https://www.bigdatacloud.com/network-engineering/bgp-active-prefixes-api) |
| [List Networks by CIDR](actions/list-networks-by-cidr.md) | `GET /data/network-by-cidr` | [docs](https://www.bigdatacloud.com/network-engineering/networks-by-cidr-api) |
| [List Tor Exit Nodes Geolocated](actions/list-tor-exit-nodes-geolocated.md) | `GET /data/tor-exit-nodes-list` | [docs](https://www.bigdatacloud.com/network-engineering/tor-exit-nodes-geolocated-api) |
| [Parse User Agent](actions/parse-user-agent.md) | `GET /data/user-agent-info` | [docs](https://www.bigdatacloud.com/ip-geolocation/user-agent-parser-api) |
| [Reverse Geocode to City](actions/reverse-geocode-to-city.md) | `GET /data/reverse-geocode` | [docs](https://www.bigdatacloud.com/reverse-geocoding/reverse-geocode-to-city-api) |
| [Reverse Geocode with Timezone](actions/reverse-geocode-with-timezone.md) | `GET /data/reverse-geocode-with-timezone` | [docs](https://www.bigdatacloud.com/reverse-geocoding/reverse-geocode-with-timezone) |
| [Validate Phone Number](actions/validate-phone-number.md) | `GET /data/phone-number-validate` | [docs](https://www.bigdatacloud.com/phone-email-verification/phone-number-validation-api) |
| [Validate Phone Number by IP](actions/validate-phone-number-by-ip.md) | `GET /data/phone-number-validate-by-ip` | [docs](https://www.bigdatacloud.com/phone-email-verification/phone-number-validation-by-ip-address-api) |
| [Verify Email Address](actions/verify-email-address.md) | `GET /data/email-verify` | [docs](https://www.bigdatacloud.com/phone-email-verification/email-verify-api) |
