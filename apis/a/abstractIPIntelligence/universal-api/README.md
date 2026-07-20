# <img src="https://images.mindcloud.co/apps/icons/images-2_1774298007987.png" alt="Abstract IP Intelligence logo" width="28" height="28"> Abstract IP Intelligence: Universal API

Analyze an IP address for geolocation, company, ASN, timezone, currency, domain, and security signals using Abstract IP Intelligence.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/abstractIPIntelligence/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.abstractapi.com
- **Vendor API docs:** https://docs.abstractapi.com/api/ip-intelligence

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get IP Intelligence](actions/get-ip-intelligence.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abstractIPIntelligence/latest/actions/get-ip-intelligence?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Ip Intelligence

| Action | Method | Description |
| --- | --- | --- |
| [Get IP Intelligence](actions/get-ip-intelligence.md) | GET | Retrieves IP intelligence from Abstract IP Intelligence. |

