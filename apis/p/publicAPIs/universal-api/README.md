# <img src="https://images.mindcloud.co/apps/icons/public-apis_1776794759091.png" alt="Public APIs logo" width="28" height="28"> Public APIs: Universal API

Browse public API resources and categories

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/publicAPIs/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://github.com/marcelscruz/public-apis
- **Vendor API docs:** https://github.com/marcelscruz/public-apis/blob/main/API.md

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Categories](actions/list-categories.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/publicAPIs/latest/actions/list-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET | Retrieves API categories from Public APIs. |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [List Entries](actions/list-entries.md) | GET | Retrieves public API entries from Public APIs. |

