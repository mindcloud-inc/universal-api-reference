# <img src="https://images.mindcloud.co/apps/icons/botmother-icon_1775162345665.png" alt="Botmother logo" width="28" height="28"> Botmother: Universal API

Trigger Botmother external events to launch a configured bot screen or message for platform users, Botmother users, or everyone.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/botmother/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://botmother.com
- **Vendor API docs:** https://docs.botmother.com/article/42097

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Trigger External Event For Botmother Users](actions/trigger-external-event-for-botmother-users.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/botmother/latest/actions/trigger-external-event-for-botmother-users" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "usersBm[]": [
    "string"
  ],
  "data": {}
}'
```

## Actions (6)

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Trigger External Event For Botmother Users](actions/trigger-external-event-for-botmother-users.md) | POST | Triggers an external event in Botmother for users by bm_id. |
| [Trigger External Event For Botmother Users And Close Dialogs](actions/trigger-external-event-for-botmother-users-and-close-dialogs.md) | POST | Triggers an external event in Botmother for users by bm_id and closes chats. |
| [Trigger External Event For Everyone](actions/trigger-external-event-for-everyone.md) | POST | Triggers an external event in Botmother for all users. |
| [Trigger External Event For Everyone And Close Dialogs](actions/trigger-external-event-for-everyone-and-close-dialogs.md) | POST | Triggers an external event in Botmother for all users and closes chats. |
| [Trigger External Event For Platform Users](actions/trigger-external-event-for-platform-users.md) | POST | Triggers an external event in Botmother for platform users. |
| [Trigger External Event For Platform Users And Close Dialogs](actions/trigger-external-event-for-platform-users-and-close-dialogs.md) | POST | Triggers an external event in Botmother for platform users and closes chats. |

