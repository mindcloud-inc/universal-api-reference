# <img src="https://images.mindcloud.co/apps/icons/favicon-api-apaleo-com-48x48_1776185227345.png" alt="Apaleo Official logo" width="28" height="28"> Apaleo Official: Universal API

Manage hotel properties, reservations, rates, and folios

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/apaleoOfficial/latest
- **Category:** Commerce / ERP
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://apaleo.com
- **Vendor API docs:** https://api.apaleo.com/swagger/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Properties](actions/list-properties.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apaleoOfficial/latest/actions/list-properties?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Property

| Action | Method | Description |
| --- | --- | --- |
| [List Properties](actions/list-properties.md) | GET | Retrieves properties from your Apaleo Official account. |

