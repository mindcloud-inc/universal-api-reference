# <img src="https://images.mindcloud.co/apps/icons/sync-mate_1775674549511.png" alt="SyncMate logo" width="28" height="28"> SyncMate: Universal API

Send automated WhatsApp messages and alerts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/syncMate/latest
- **Category:** Marketing
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://assistro.co/
- **Vendor API docs:** https://assistro.co/user-guide/developer-guide/connect-your-custom-app-with-syncmate/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Connection](actions/check-connection.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syncMate/latest/actions/check-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Check Connection](actions/check-connection.md) | GET |  |
| [Check WhatsApp Number](actions/check-whats-app-number.md) | GET |  |
| [Connect WhatsApp Session](actions/connect-whats-app-session.md) | POST |  |
| [Disconnect WhatsApp Session](actions/disconnect-whats-app-session.md) | DELETE |  |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Get Group Participants](actions/get-group-participants.md) | GET |  |
| [Get Groups](actions/get-groups.md) | GET |  |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Bulk Message](actions/send-bulk-message.md) | POST |  |
| [Send Message To A Channel/Newsletter Via SyncMate](actions/send-message-to-a-channel-newsletter-via-sync-mate.md) | POST |  |
| [Send Single Message](actions/send-single-message.md) | POST |  |
| [Send WhatsApp Group Message Via SyncMate](actions/send-whats-app-group-message-via-sync-mate.md) | POST |  |

