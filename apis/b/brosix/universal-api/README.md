# <img src="https://images.mindcloud.co/apps/icons/images_1774971970375.png" alt="Brosix logo" width="28" height="28"> Brosix: Universal API

Brosix: Send team chat notifications to users and chat rooms

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/brosix/latest
- **Category:** Communication / Team Messaging
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.brosix.com/
- **Vendor API docs:** https://help.brosix.com/notifications-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Send Message](actions/send-message.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/brosix/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": "MindCloud test message"
}'
```

## Actions (1)

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Message](actions/send-message.md) | POST | Creates a new message in Brosix for a user or chat room. |

