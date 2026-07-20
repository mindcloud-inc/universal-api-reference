# <img src="https://images.mindcloud.co/apps/icons/images-6_1774881096736.png" alt="Pushinator logo" width="28" height="28"> Pushinator: Universal API

Send mobile notifications and manage Pushinator channels

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pushinator/latest
- **Category:** Communication / Team Messaging
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pushinator.com
- **Vendor API docs:** https://pushinator.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushinator/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [List Channels](actions/list-channels.md) | GET | Retrieves all available channels from Pushinator. |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [Send Notification](actions/send-notification.md) | POST | Creates a new notification in a Pushinator channel. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Pushinator. |

