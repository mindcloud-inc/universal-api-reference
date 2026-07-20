# <img src="https://images.mindcloud.co/apps/icons/mozilla-observatory_1776195186694.png" alt="Mozilla Observatory logo" width="28" height="28"> Mozilla Observatory: Universal API

Scan websites for HTTP security issues

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mozillaObservatory/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://developer.mozilla.org/en-US/observatory
- **Vendor API docs:** https://developer.mozilla.org/en-US/observatory/docs/faq

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Scan website](actions/scan-website.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mozillaObservatory/latest/actions/scan-website" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "host": "example.com"
}'
```

## Actions (1)

### Website

| Action | Method | Description |
| --- | --- | --- |
| [Scan website](actions/scan-website.md) | POST | Creates a new website scan in Mozilla Observatory. |

