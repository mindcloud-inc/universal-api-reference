# <img src="https://images.mindcloud.co/apps/icons/i-pinfo_1774272698909.png" alt="IPInfo logo" width="28" height="28"> IPInfo: Universal API

Analyze IPs, geolocation, ASN, and network intelligence

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/iPInfo/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ipinfo.io
- **Vendor API docs:** https://ipinfo.io/developers

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Lite My IP Details](actions/get-lite-my-ip-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPInfo/latest/actions/get-lite-my-ip-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Batch Lite IP Lookups](actions/batch-lite-ip-lookups.md) | GET |  |
| [Get Lite IP Details](actions/get-lite-ip-details.md) | GET |  |
| [Get Lite IP Field](actions/get-lite-ip-field.md) | GET |  |
| [Get Lite My IP Details](actions/get-lite-my-ip-details.md) | GET |  |
| [Get Lite My IP Field](actions/get-lite-my-ip-field.md) | GET |  |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Create IP Map](actions/create-ip-map.md) | POST |  |

