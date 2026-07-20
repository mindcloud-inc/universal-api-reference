# <img src="https://images.mindcloud.co/apps/icons/kick-fire_1775158843293.png" alt="KickFire logo" width="28" height="28"> KickFire: Universal API

KickFire enriches IP addresses and domains with company firmographic data and API usage insights through Foundry's developer APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kickFire/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://kickfire.com
- **Vendor API docs:** https://foundryco.com/developers/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company by Website](actions/get-company-by-website.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kickFire/latest/actions/get-company-by-website?connectionId=$CONNECTION_ID&website=example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Api Usage Report

| Action | Method | Description |
| --- | --- | --- |
| [Get API Usage](actions/get-api-usage.md) | GET | Retrieves API usage information from KickFire. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company by IP Address](actions/get-company-by-ip-address.md) | GET | Retrieves company firmographic data from KickFire by IP address. |
| [Get Company by Website](actions/get-company-by-website.md) | GET | Retrieves company firmographic data from KickFire by website. |

### Myapi Data

| Action | Method | Description |
| --- | --- | --- |
| [Get My API Data](actions/get-my-api-data.md) | GET | Retrieves MyAPI custom account attributes from KickFire. |

