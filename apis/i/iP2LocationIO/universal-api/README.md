# <img src="https://images.mindcloud.co/apps/icons/i-p2location-io_1774273049765.png" alt="IP2Location IO logo" width="28" height="28"> IP2Location IO: Universal API

Look up IP geolocation and network details

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/iP2LocationIO/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ip2location.io/
- **Vendor API docs:** https://www.ip2location.io/ip2location-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get IP Geolocation](actions/get-ip-geolocation.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iP2LocationIO/latest/actions/get-ip-geolocation?connectionId=$CONNECTION_ID&ip=8.8.8.8" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Ip Address

| Action | Method | Description |
| --- | --- | --- |
| [Get IP Geolocation](actions/get-ip-geolocation.md) | GET |  |

