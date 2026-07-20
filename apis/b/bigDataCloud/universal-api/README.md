# <img src="https://images.mindcloud.co/apps/icons/big-data-cloud_1775669194024.png" alt="BigDataCloud logo" width="28" height="28"> BigDataCloud: Universal API

Geolocate IPs and enrich location, network, phone, and email data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bigDataCloud/latest
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.bigdatacloud.com/
- **Vendor API docs:** https://www.bigdatacloud.com/support/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get IP Geolocation Report](actions/get-ip-geolocation.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/get-ip-geolocation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Asn

| Action | Method | Description |
| --- | --- | --- |
| [Get ASN Info Extended](actions/get-asn-info-extended.md) | GET | Retrieves extended ASN details from BigDataCloud. |

### Asn Rank List

| Action | Method | Description |
| --- | --- | --- |
| [List ASN Ranks](actions/list-asn-ranks.md) | GET | Retrieves ASN rank data from BigDataCloud. |

### Asn Receiving From

| Action | Method | Description |
| --- | --- | --- |
| [Get ASN Receiving From](actions/get-asn-receiving-from.md) | GET | Retrieves ASN receiving-from information from BigDataCloud. |

### Asn Transit To

| Action | Method | Description |
| --- | --- | --- |
| [Get ASN Transit To](actions/get-asn-transit-to.md) | GET | Retrieves ASN transit-to information from BigDataCloud. |

### Bgp Prefix List

| Action | Method | Description |
| --- | --- | --- |
| [List BGP Active Prefixes](actions/list-bgp-active-prefixes.md) | GET | Retrieves active BGP prefixes from BigDataCloud. |

### Ip Geolocation

| Action | Method | Description |
| --- | --- | --- |
| [Get IP Geolocation with Confidence Area](actions/get-ip-geolocation-with-confidence-area.md) | GET | Retrieves IP geolocation with confidence area details from BigDataCloud. |

### Ip Geolocation Report

| Action | Method | Description |
| --- | --- | --- |
| [Get IP Geolocation Report](actions/get-ip-geolocation.md) | GET | Retrieves IP geolocation, confidence area, and hazard details from BigDataCloud. |

### Ipv4 Address Space Monitoring

| Action | Method | Description |
| --- | --- | --- |
| [Get IPv4 Address Space Monitoring](actions/get-ipv4-address-space-monitoring.md) | GET | Retrieves IPv4 address space monitoring data from BigDataCloud. |

### Network List

| Action | Method | Description |
| --- | --- | --- |
| [List Networks by CIDR](actions/list-networks-by-cidr.md) | GET | Retrieves network details by CIDR from BigDataCloud. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get ASN Info](actions/get-asn-info.md) | GET | Retrieves ASN details from BigDataCloud. |
| [Get Country by IP](actions/get-country-by-ip.md) | GET | Retrieves country details by IP address from BigDataCloud. |
| [Get Country Info](actions/get-country-info.md) | GET | Retrieves country information from BigDataCloud. |
| [Get Hazard Report](actions/get-hazard-report.md) | GET | Retrieves hazard report details from BigDataCloud. |
| [Get IP Geolocation](actions/get-ip-geolocation-basic.md) | GET | Retrieves IP geolocation details from BigDataCloud. |
| [Get Network by IP](actions/get-network-by-ip.md) | GET | Retrieves network details by IP address from BigDataCloud. |
| [Get Time Zone by IP](actions/get-time-zone-by-ip.md) | GET | Retrieves time zone details by IP address from BigDataCloud. |
| [Get Time Zone by Location](actions/get-time-zone-by-location.md) | GET | Retrieves time zone details by location from BigDataCloud. |
| [Get Time Zone Info](actions/get-time-zone-info.md) | GET | Retrieves time zone information from BigDataCloud. |
| [Get User Risk](actions/get-user-risk.md) | GET | Retrieves user risk details from BigDataCloud. |
| [Parse User Agent](actions/parse-user-agent.md) | GET | Parses a user agent in BigDataCloud. |
| [Reverse Geocode to City](actions/reverse-geocode-to-city.md) | GET | Reverse geocodes coordinates to a city in BigDataCloud. |
| [Reverse Geocode with Timezone](actions/reverse-geocode-with-timezone.md) | GET | Reverse geocodes coordinates with timezone details in BigDataCloud. |
| [Validate Phone Number](actions/validate-phone-number.md) | GET | Validates a phone number in BigDataCloud. |
| [Verify Email Address](actions/verify-email-address.md) | GET | Verifies an email address in BigDataCloud. |

### Phone Number Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Phone Number by IP](actions/validate-phone-number-by-ip.md) | GET | Validates a phone number by IP address in BigDataCloud. |

### Tor Exit Node List

| Action | Method | Description |
| --- | --- | --- |
| [List Tor Exit Nodes Geolocated](actions/list-tor-exit-nodes-geolocated.md) | GET | Retrieves geolocated Tor exit nodes from BigDataCloud. |

