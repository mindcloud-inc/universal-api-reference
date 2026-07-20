# <img src="https://images.mindcloud.co/apps/icons/activity-smith_1775134814473.png" alt="ActivitySmith logo" width="28" height="28"> ActivitySmith: Universal API

Send push notifications and manage iOS Live Activities

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/activitySmith/latest
- **Category:** Communication / Team Messaging
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://activitysmith.com
- **Vendor API docs:** https://activitysmith.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [End Live Activity](actions/end-live-activity.md):

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/activitySmith/latest/actions/end-live-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "activityId": "string"
}'
```

## Actions (4)

### Live Activity

| Action | Method | Description |
| --- | --- | --- |
| [End Live Activity](actions/end-live-activity.md) | PUT | Ends an existing Live Activity in ActivitySmith. |
| [Start Live Activity](actions/start-live-activity.md) | POST | Creates a Live Activity in ActivitySmith. |
| [Update Live Activity](actions/update-live-activity.md) | PUT | Updates an existing Live Activity in ActivitySmith. |

### Push Notification

| Action | Method | Description |
| --- | --- | --- |
| [Send Push Notification](actions/send-push-notification.md) | POST | Sends a push notification in ActivitySmith. |

