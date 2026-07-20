# <img src="https://images.mindcloud.co/apps/icons/discord_1772571161467.png" alt="Discord logo" width="28" height="28"> Discord: Universal API

Chat, call, stream, and build communities across Discord servers.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/discord/latest
- **Category:** Communication / Team Messaging
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://discord.com/
- **Vendor API docs:** https://docs.discord.com/developers/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discord/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel](actions/get-channel.md) | GET | Retrieves a Discord channel by ID. |
| [List Guild Channels](actions/list-guild-channels.md) | GET | Lists channels in a Discord guild. |
| [Trigger Typing Indicator](actions/trigger-typing-indicator.md) | POST | Triggers a typing indicator in a Discord channel. |

### Guild

| Action | Method | Description |
| --- | --- | --- |
| [List Current User Guilds](actions/list-current-user-guilds.md) | GET | Lists the current user's guilds in Discord. |

### Guild Ban

| Action | Method | Description |
| --- | --- | --- |
| [Create Guild Ban](actions/create-guild-ban.md) | POST | Creates a guild ban in Discord. |
| [Remove Guild Ban](actions/remove-guild-ban.md) | DELETE | Removes a guild ban in Discord. |

### Guild Member

| Action | Method | Description |
| --- | --- | --- |
| [Get Guild Member](actions/get-guild-member.md) | GET | Retrieves a Discord guild member by user ID. |
| [List Guild Members](actions/list-guild-members.md) | GET | Lists members in a Discord guild. |
| [Remove Guild Member](actions/remove-guild-member.md) | DELETE | Removes a member from a Discord guild. |
| [Update Guild Member](actions/update-guild-member.md) | PUT | Updates a member in a Discord guild. |

### Guild Role

| Action | Method | Description |
| --- | --- | --- |
| [Create Guild Role](actions/create-guild-role.md) | POST | Creates a new role in a Discord guild. |
| [Delete Guild Role](actions/delete-guild-role.md) | DELETE | Deletes a role from a Discord guild. |
| [List Guild Roles](actions/list-guild-roles.md) | GET | Lists roles in a Discord guild. |
| [Update Guild Role](actions/update-guild-role.md) | PUT | Updates a role in a Discord guild. |

### Interaction Response

| Action | Method | Description |
| --- | --- | --- |
| [Create Interaction Response](actions/create-interaction-response.md) | POST | Creates an interaction response in Discord. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Create Message](actions/create-message.md) | POST | Creates a message in a Discord channel. |
| [Delete Message](actions/delete-message.md) | DELETE | Deletes a message from a Discord channel. |
| [List Messages](actions/list-messages.md) | GET | Lists messages in a Discord channel. |
| [Update Message](actions/update-message.md) | PUT | Updates a message in a Discord channel. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Delete Messages](actions/bulk-delete-messages.md) | DELETE | Deletes multiple messages from a Discord channel. |
| [Create Reaction](actions/create-reaction.md) | POST | Creates a reaction on a Discord message. |
| [Delete Own Reaction](actions/delete-own-reaction.md) | DELETE | Deletes the current user's reaction from a Discord message. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current authenticated Discord user. |

