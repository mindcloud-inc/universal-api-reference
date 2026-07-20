# <img src="https://images.mindcloud.co/apps/icons/stream_1774629496821.png" alt="Stream logo" width="28" height="28"> Stream: Universal API

Manage Stream chat users, channels, messages, and moderation

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/stream/latest
- **Category:** Communication / Team Messaging
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://getstream.io/
- **Vendor API docs:** https://getstream.io/chat/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get App Settings](actions/get-app-settings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stream/latest/actions/get-app-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Get App Settings](actions/get-app-settings.md) | GET | Retrieves app settings from Stream. |

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [Get Or Create Channel](actions/get-or-create-channel.md) | POST | Finds a channel in Stream, or creates it if needed. |
| [Hide Channel](actions/hide-channel.md) | PUT | Hides a channel in Stream. |
| [Search Channels](actions/search-channels.md) | GET | Finds channels in Stream by filter criteria. |
| [Show Channel](actions/show-channel.md) | PUT | Shows a hidden channel in Stream. |
| [Update Channel](actions/update-channel.md) | PUT | Updates an existing channel in Stream. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Send User Event](actions/send-user-event.md) | POST | Sends a custom event to a user in Stream. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Create Poll](actions/create-poll.md) | POST | Creates a new poll in Stream. |
| [Search Polls](actions/search-polls.md) | GET | Finds polls in Stream by filter criteria. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Delete Message](actions/delete-message.md) | DELETE | Deletes an existing message from Stream. |
| [Get Message](actions/get-message.md) | GET | Retrieves a message from Stream. |
| [List Channel Messages](actions/list-channel-messages.md) | GET | Retrieves messages from a specific channel in Stream. |
| [List Message Replies](actions/list-message-replies.md) | GET | Retrieves replies from a message thread in Stream. |
| [Search Messages](actions/search-messages.md) | GET | Finds messages in Stream by search criteria. |
| [Send Message](actions/send-message.md) | POST | Creates a new message in Stream. |
| [Update Message](actions/update-message.md) | PUT | Updates an existing message in Stream. |

### Reactions

| Action | Method | Description |
| --- | --- | --- |
| [Delete Reaction](actions/delete-reaction.md) | DELETE | Deletes a reaction from a Stream message. |
| [Send Reaction](actions/send-reaction.md) | POST | Creates a reaction for a Stream message. |

### Threads

| Action | Method | Description |
| --- | --- | --- |
| [Search Threads](actions/search-threads.md) | GET | Finds threads in Stream by filter criteria. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Ban User](actions/ban-user.md) | PUT | Bans a user in Stream. |
| [Deactivate User](actions/deactivate-user.md) | PUT | Deactivates a user in Stream. |
| [Reactivate User](actions/reactivate-user.md) | PUT | Reactivates a user in Stream. |
| [Unban User](actions/unban-user.md) | PUT | Unbans a user in Stream. |
| [Upsert Users](actions/upsert-users.md) | PUT | Creates or updates users in Stream. |

