# <img src="https://images.mindcloud.co/apps/icons/hook-notifier_1776088205081.png" alt="Hook.Notifier logo" width="28" height="28"> Hook.Notifier: Universal API

Collect webhook-powered notifications and manage them in the Hook.Notifier inbox.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hookNotifier/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://hooknotifier.com/
- **Vendor API docs:** https://hooknotifier.com/blog/get-started-with-hook-notifier

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Send Notification](actions/send-notification.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hookNotifier/latest/actions/send-notification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "object": "string",
  "body": "string"
}'
```

## Actions (2)

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [Send Notification](actions/send-notification.md) | POST | Sends a custom notification through Hook.Notifier. |
| [Verify Connection](actions/verify-connection.md) | POST | Sends a fixed test notification through Hook.Notifier. |

