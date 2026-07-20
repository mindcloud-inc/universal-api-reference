# <img src="https://images.mindcloud.co/apps/icons/pusher_1774361394311.png" alt="Pusher logo" width="28" height="28"> Pusher: Universal API

Pusher Channels is a realtime messaging platform for publishing events to channels and reading channel and user state through the Channels HTTP API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pusher/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pusher.com/
- **Vendor API docs:** https://pusher.com/docs/channels/library_auth_reference/rest-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Channels](actions/list-channels.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pusher/latest/actions/list-channels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel](actions/get-channel.md) | GET | Retrieves channel details from Pusher. |
| [List Channels](actions/list-channels.md) | GET | Retrieves channels from Pusher. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Trigger Batch Events](actions/trigger-batch-events.md) | POST | Triggers multiple events in Pusher. |
| [Trigger Event](actions/trigger-event.md) | POST | Triggers an event in Pusher. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Channel Users](actions/list-channel-users.md) | GET | Retrieves users from a Pusher presence channel. |
| [Terminate User Connections](actions/terminate-user-connections.md) | DELETE | Terminates a user's connections in Pusher. |

