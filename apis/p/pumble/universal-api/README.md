# <img src="https://images.mindcloud.co/apps/icons/pumble_1773779953861.png" alt="Pumble logo" width="28" height="28"> Pumble: Universal API

Send messages, manage channels, and schedule posts in Pumble

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pumble/latest
- **Category:** Communication / Team Messaging
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pumble.com
- **Vendor API docs:** https://pumble-api-keys.addons.marketplace.cake.com/api-docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pumble/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Create Channel](actions/create-channel.md) | POST | Creates a new channel in Pumble. |
| [Get Channel](actions/get-channel.md) | GET | Retrieves a channel from Pumble by ID or name. |
| [List Channels](actions/list-channels.md) | GET | Retrieves channels from Pumble. |

### Channel Membership

| Action | Method | Description |
| --- | --- | --- |
| [Add Users to Channel](actions/add-users-to-channel.md) | POST | Adds users to a Pumble channel. |
| [Remove User from Channel](actions/remove-user-from-channel.md) | DELETE | Removes a user from a Pumble channel. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [List User Groups](actions/list-user-groups.md) | GET | Retrieves user groups from a Pumble workspace. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Delete Message](actions/delete-message.md) | DELETE | Deletes a message from Pumble. |
| [Get Message](actions/get-message.md) | GET | Retrieves a message from Pumble by ID. |
| [List Channel Messages](actions/list-channel-messages.md) | GET | Retrieves messages from a Pumble channel. |
| [List Thread Replies](actions/list-thread-replies.md) | GET | Retrieves replies for a Pumble thread message. |
| [Reply to Message](actions/reply-to-message.md) | POST | Creates a reply to a Pumble channel message. |
| [Search Messages](actions/search-messages.md) | GET | Finds messages in Pumble by search criteria. |
| [Send Direct Message to Group](actions/send-direct-message-to-group.md) | POST | Creates a direct message to a Pumble user group. |
| [Send Direct Message to User](actions/send-direct-message-to-user.md) | POST | Creates a direct message to a Pumble user. |
| [Send Message to Channel](actions/send-message-to-channel.md) | POST | Creates a new message in a Pumble channel. |
| [Update Message](actions/update-message.md) | PUT | Updates the text of a Pumble message. |

### Reaction

| Action | Method | Description |
| --- | --- | --- |
| [Add Reaction to Message](actions/add-reaction-to-message.md) | POST | Adds a reaction to a Pumble message. |

### Scheduled Message

| Action | Method | Description |
| --- | --- | --- |
| [Create Scheduled Message](actions/create-scheduled-message.md) | POST | Creates a scheduled message in Pumble. |
| [Delete Scheduled Message](actions/delete-scheduled-message.md) | DELETE | Deletes a scheduled message from Pumble. |
| [Get Scheduled Message](actions/get-scheduled-message.md) | GET | Retrieves a scheduled message from Pumble by ID. |
| [List Scheduled Messages](actions/list-scheduled-messages.md) | GET | Retrieves scheduled messages from Pumble. |
| [Update Scheduled Message](actions/update-scheduled-message.md) | PUT | Updates an existing scheduled message in Pumble. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves current user details from Pumble. |
| [List Users](actions/list-users.md) | GET | Retrieves users from a Pumble workspace. |

