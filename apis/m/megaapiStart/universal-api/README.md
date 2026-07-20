# <img src="https://images.mindcloud.co/apps/icons/favicon-doc-mega-api-app-br-48x48_1776106574565.png" alt="Megaapi Start logo" width="28" height="28"> Megaapi Start: Universal API

Send WhatsApp messages, manage instances, webhooks, chats, and groups

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/megaapiStart/latest
- **Category:** Support / Contact Center
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://megaapi.io
- **Vendor API docs:** https://doc.mega-api.app.br

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Connection Status](actions/get-connection-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/megaapiStart/latest/actions/get-connection-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Connection Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Connection Status](actions/get-connection-status.md) | GET | Retrieves WhatsApp connection status from Megaapi Start. |

