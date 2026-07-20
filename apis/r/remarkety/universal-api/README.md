# <img src="https://images.mindcloud.co/apps/icons/remarkety_1775664153606.png" alt="Remarkety logo" width="28" height="28"> Remarkety: Universal API

Email and SMS marketing automation platform for ecommerce stores, including custom API endpoints for syncing contacts and marketing subscription state.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/remarkety/latest
- **Category:** Marketing
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.remarkety.com
- **Vendor API docs:** https://support.remarkety.com/hc/en-us/articles/115005328223-Remarkety-Custom-API-V2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Batch Upsert Contacts](actions/batch-upsert-contacts.md):

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/remarkety/latest/actions/batch-upsert-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contacts[]": [
    {}
  ]
}'
```

## Actions (3)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Batch Upsert Contacts](actions/batch-upsert-contacts.md) | PUT |  |
| [Unsubscribe Contact](actions/unsubscribe-contact.md) | PUT |  |
| [Upsert Contact](actions/upsert-contact.md) | PUT |  |

