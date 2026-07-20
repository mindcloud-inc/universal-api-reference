# <img src="https://images.mindcloud.co/apps/icons/mapsly_1775749775738.png" alt="Mapsly logo" width="28" height="28"> Mapsly: Universal API

Mapsly offers write-focused API endpoints for creating, updating, and deleting entity records in Mapsly data sources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mapsly/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mapsly.com
- **Vendor API docs:** https://developer.mapsly.com/docs/api/ZG9jOjc1MTcyMDI-introduction-to-mapsly-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Upsert Record Using GET](actions/upsert-record-using-get.md):

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mapsly/latest/actions/upsert-record-using-get" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entity": "string",
  "id": "string"
}'
```

## Actions (6)

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Delete Record Using GET](actions/delete-record-using-get.md) | DELETE | Deletes a record from Mapsly using GET. |
| [Delete Record Using POST](actions/delete-record-using-post.md) | DELETE | Deletes a record from Mapsly using POST. |
| [Delete Records](actions/delete-records.md) | DELETE | Deletes records from Mapsly. |
| [Upsert Record Using GET](actions/upsert-record-using-get.md) | PUT | Creates or updates a record in Mapsly using GET. |
| [Upsert Record Using POST](actions/upsert-record-using-post.md) | PUT | Creates or updates a record in Mapsly using POST. |
| [Upsert Records](actions/upsert-records.md) | PUT | Creates or updates records in Mapsly. |

