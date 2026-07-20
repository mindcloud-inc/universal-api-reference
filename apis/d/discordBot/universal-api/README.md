# <img src="https://images.mindcloud.co/apps/icons/toppng_1778014226245.png" alt="Discord-Bot logo" width="28" height="28"> Discord-Bot: Universal API

Operate Discord as a bot through the Discord REST API for server, channel, message, member, role, invite, webhook, and thread workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/discordBot/latest
- **Category:** Communication / Team Messaging
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://discord.com
- **Vendor API docs:** https://docs.discord.com/developers/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Bot User](actions/get-current-bot-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/get-current-bot-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Create Guild Channel](actions/create-guild-channel.md) | POST | Creates a channel in a Discord guild. |
| [Delete Channel](actions/delete-channel.md) | DELETE | Deletes or closes a Discord channel. |
| [Get Channel](actions/get-channel.md) | GET | Retrieves a Discord channel by ID. |
| [List Guild Channels](actions/list-guild-channels.md) | GET | Retrieves channels for a Discord guild. |
| [Update Channel](actions/update-channel.md) | PUT | Updates an existing channel in Discord. |

### Guild

| Action | Method | Description |
| --- | --- | --- |
| [Get Guild](actions/get-guild.md) | GET | Retrieves a Discord guild by ID. |

### Guild Member

| Action | Method | Description |
| --- | --- | --- |
| [Get Guild Member](actions/get-guild-member.md) | GET | Retrieves a member from a Discord guild. |
| [List Guild Members](actions/list-guild-members.md) | GET | Retrieves members from a Discord guild. |
| [Search Guild Members](actions/search-guild-members.md) | GET | Finds Discord guild members by username or nickname prefix. |

### Guild Member Role

| Action | Method | Description |
| --- | --- | --- |
| [Add Guild Member Role](actions/add-guild-member-role.md) | POST | Adds a role to a Discord guild member. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Delete Messages](actions/bulk-delete-messages.md) | DELETE | Deletes multiple messages from a Discord channel. |
| [Create Message](actions/create-message.md) | POST | Creates a message in a Discord channel. |
| [Delete Message](actions/delete-message.md) | DELETE | Deletes a message from a Discord channel. |
| [Edit Message](actions/edit-message.md) | PUT | Updates an existing message in Discord. |
| [Get Channel Message](actions/get-channel-message.md) | GET | Retrieves a specific message from Discord. |
| [List Channel Messages](actions/list-channel-messages.md) | GET | Retrieves messages from a Discord channel. |

### Reaction

| Action | Method | Description |
| --- | --- | --- |
| [Create Reaction](actions/create-reaction.md) | POST | Creates a reaction on a Discord message. |
| [Delete Own Reaction](actions/delete-own-reaction.md) | DELETE | Deletes the bot's reaction from a Discord message. |
| [Get Reactions](actions/get-reactions.md) | GET | Retrieves users who reacted to a Discord message. |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [Create Guild Role](actions/create-guild-role.md) | POST | Creates a role in a Discord guild. |
| [Delete Guild Role](actions/delete-guild-role.md) | DELETE | Deletes a role from a Discord guild. |
| [List Guild Roles](actions/list-guild-roles.md) | GET | Retrieves roles from a Discord guild. |

### Typing Indicator

| Action | Method | Description |
| --- | --- | --- |
| [Trigger Typing Indicator](actions/trigger-typing-indicator.md) | POST | Triggers a typing indicator in a Discord channel. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Bot User](actions/get-current-bot-user.md) | GET | Retrieves the current bot user from Discord. |

