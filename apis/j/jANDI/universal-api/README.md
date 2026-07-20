# <img src="https://images.mindcloud.co/apps/icons/j-andi_1774294039844.png" alt="JANDI logo" width="28" height="28"> JANDI: Universal API

Send JANDI messages through incoming webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/jANDI/latest
- **Category:** Communication / Team Messaging
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.jandi.com/landing/en
- **Vendor API docs:** https://support.jandi.com/en/categories/Connect-3c9dda43

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Send Incoming Webhook Message](actions/send-incoming-webhook-message.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jANDI/latest/actions/send-incoming-webhook-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": "MindCloud test message"
}'
```

## Actions (1)

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Send Incoming Webhook Message](actions/send-incoming-webhook-message.md) | POST |  |

