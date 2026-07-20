# <img src="https://images.mindcloud.co/apps/icons/favicon-green-api-com-48x48_1776103095950.png" alt="GREEN-API for WhatsApp logo" width="28" height="28"> GREEN-API for WhatsApp: Universal API

Send WhatsApp messages, manage chats, and control GREEN-API instances

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gREENAPIForWhatsApp/latest
- **Category:** Communication / Team Messaging
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://green-api.com
- **Vendor API docs:** https://green-api.com/en/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Instance State](actions/get-instance-state.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gREENAPIForWhatsApp/latest/actions/get-instance-state?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Get Instance State](actions/get-instance-state.md) | GET | Retrieves the WhatsApp instance state from GREEN-API. |

