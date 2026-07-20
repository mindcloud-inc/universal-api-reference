# <img src="https://images.mindcloud.co/apps/icons/adalo_1773262932591.png" alt="Adalo logo" width="28" height="28"> Adalo: Universal API

Manage Adalo app data and send push notifications

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/adalo/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.adalo.com
- **Vendor API docs:** https://help.adalo.com/integrations/the-adalo-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Collection Records](actions/list-collection-records.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adalo/latest/actions/list-collection-records?connectionId=$CONNECTION_ID&limit=25&offset=0&appId=string&collectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Collection Record

| Action | Method | Description |
| --- | --- | --- |
| [List Collection Records](actions/list-collection-records.md) | GET | Retrieves records from a specific Adalo collection. |

