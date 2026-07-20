# <img src="https://images.mindcloud.co/apps/icons/images_1773753906406.png" alt="ProveSource logo" width="28" height="28"> ProveSource: Universal API

Capture social-proof events and power real-time website notifications for conversions, stream activity, and related proof experiences.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/proveSource/latest
- **Category:** Marketing
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://provesrc.com/
- **Vendor API docs:** https://help.provesrc.com/en/collections/2021450-webhooks

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Send Webhook Event](actions/send-webhook-event.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/proveSource/latest/actions/send-webhook-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookId": "string"
}'
```

## Actions (1)

### Webhook Event

| Action | Method | Description |
| --- | --- | --- |
| [Send Webhook Event](actions/send-webhook-event.md) | POST |  |

