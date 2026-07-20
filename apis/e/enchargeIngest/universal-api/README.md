# Encharge Ingest: Universal API

Encharge Ingest sends people updates and event data from your backend into Encharge through the single-endpoint Ingest API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/enchargeIngest/latest
- **Category:** Marketing
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://encharge.io/
- **Vendor API docs:** https://docs.encharge.io/getting-started/connecting-your-app-to-encharge/ingest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Alias Person](actions/alias-person.md):

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/enchargeIngest/latest/actions/alias-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "user": {}
}'
```

## Actions (4)

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Send Event](actions/send-event.md) | POST |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Alias Person](actions/alias-person.md) | PUT |  |
| [Group Object](actions/group-object.md) | POST |  |
| [Identify Person](actions/identify-person.md) | PUT |  |

