# <img src="https://images.mindcloud.co/apps/icons/uchat_1776358060100.png" alt="Uchat logo" width="28" height="28"> Uchat: Universal API

Send Uchat plugin messages to website chat rooms

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/uchat/latest
- **Category:** Communication / Team Messaging
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://uchat.io
- **Vendor API docs:** https://uchat.io/doc/2/API

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Send Plugin Message](actions/send-plugin-message.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uchat/latest/actions/send-plugin-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payload[]": "123456789123",
  "pluginId": "youtube"
}'
```

## Actions (1)

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Send Plugin Message](actions/send-plugin-message.md) | POST | Sends an array-wrapped message payload to a Uchat plugin. |

