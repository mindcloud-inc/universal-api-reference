# <img src="https://mindcloud.imgix.net/apps/icons/ping-bell_1774277523448.png" alt="PingBell logo" width="28" height="28"> PingBell: Universal API

List PingBells and send team notifications

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pingBell/latest
- **Category:** Communication / Team Messaging
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pingbell.io/
- **Vendor API docs:** https://pingbell.io/docs/pingbell-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List PingBells](actions/list-pingbells.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pingBell/latest/actions/list-pingbells?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [Send Notification](actions/send-notification.md) | POST | Creates a notification for a specific PingBell. |

### Pingbell

| Action | Method | Description |
| --- | --- | --- |
| [List PingBells](actions/list-pingbells.md) | GET | Retrieves PingBells from your PingBell account. |

