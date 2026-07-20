# <img src="https://images.mindcloud.co/apps/icons/push-by-techulus_1773855173873.png" alt="Push by Techulus logo" width="28" height="28"> Push by Techulus: Universal API

Send push notifications to linked devices and teams through Techulus Push using API-key authenticated notification and lightweight team-management endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pushByTechulus/latest
- **Category:** Communication / Team Messaging
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://push.techulus.com/
- **Vendor API docs:** https://docs.push.techulus.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Invite User to Team](actions/invite-user-to-team.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pushByTechulus/latest/actions/invite-user-to-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "team": "string",
  "email": "ava@example.com"
}'
```

## Actions (7)

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Notification](actions/send-notification.md) | POST |  |
| [Send Notification Async](actions/send-notification-async.md) | POST |  |
| [Send Notification to Device Group](actions/send-notification-to-device-group.md) | POST |  |
| [Send Notification via GET](actions/send-notification-via-get.md) | POST |  |
| [Send Notification via Path API Key](actions/send-notification-via-path-api-key.md) | POST |  |

### Team Invite

| Action | Method | Description |
| --- | --- | --- |
| [Delete Invite or Team Member](actions/delete-invite-or-team-member.md) | DELETE |  |
| [Invite User to Team](actions/invite-user-to-team.md) | POST |  |

