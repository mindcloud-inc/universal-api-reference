# <img src="https://images.mindcloud.co/apps/icons/i-p2locationio-ipgeolocation-api_1776089333373.png" alt="IP2Location.io IP Geolocation logo" width="28" height="28"> IP2Location.io IP Geolocation: Universal API

Look up IP geolocation, domain WHOIS, and hosted domains by IP with IP2Location.io and IP2WHOIS. Bulk IP geolocation is available on supported provider plans.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/iP2LocationioIPGeolocationAPI/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ip2location.io
- **Vendor API docs:** https://www.ip2location.io/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get IP Geolocation](actions/get-ip-geolocation.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iP2LocationioIPGeolocationAPI/latest/actions/get-ip-geolocation?connectionId=$CONNECTION_ID&ip=8.8.8.8" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Hosted Domain Result

| Action | Method | Description |
| --- | --- | --- |
| [List Hosted Domains by IP](actions/list-hosted-domains-by-ip.md) | GET | Retrieves hosted domains from IP2Location.io by IP address. |

### Ip Address

| Action | Method | Description |
| --- | --- | --- |
| [Get IP Geolocation](actions/get-ip-geolocation.md) | GET | Retrieves IP geolocation details from IP2Location.io. |

### Whois Record

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Domain WHOIS](actions/lookup-domain-whois.md) | GET | Retrieves domain WHOIS details from IP2Location.io by domain name. |

