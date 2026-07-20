# Discord-Bot: Native API Reference

A consolidated summary of Discord-Bot's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.discord.com/developers/reference
- **API base URL:** `https://discord.com/api/v10`

## Authentication

### Bot Token

Use a Discord bot token without the Bot prefix. MindCloud sends it as Authorization: Bot <token>.

### Credentials

- **Bot Token:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.discord.com/developers/platform/oauth2-and-permissions)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `before` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Guild Member Role](actions/add-guild-member-role.md) | `PUT /guilds/:guildId/members/:userId/roles/:roleId` | [docs](https://docs.discord.com/developers/resources/guild#add-guild-member-role) |
| [Bulk Delete Messages](actions/bulk-delete-messages.md) | `POST /channels/:channelId/messages/bulk-delete` | [docs](https://docs.discord.com/developers/resources/message#bulk-delete-messages) |
| [Create Guild Channel](actions/create-guild-channel.md) | `POST /guilds/:guildId/channels` | [docs](https://docs.discord.com/developers/resources/guild#create-guild-channel) |
| [Create Guild Role](actions/create-guild-role.md) | `POST /guilds/:guildId/roles` | [docs](https://docs.discord.com/developers/resources/guild#create-guild-role) |
| [Create Message](actions/create-message.md) | `POST /channels/:channelId/messages` | [docs](https://docs.discord.com/developers/resources/message#create-message) |
| [Create Reaction](actions/create-reaction.md) | `PUT /channels/:channelId/messages/:messageId/reactions/:emojiName/@me` | [docs](https://docs.discord.com/developers/resources/message#create-reaction) |
| [Delete Channel](actions/delete-channel.md) | `DELETE /channels/:channelId` | [docs](https://docs.discord.com/developers/resources/channel#deleteclose-channel) |
| [Delete Guild Role](actions/delete-guild-role.md) | `DELETE /guilds/:guildId/roles/:roleId` | [docs](https://docs.discord.com/developers/resources/guild#delete-guild-role) |
| [Delete Message](actions/delete-message.md) | `DELETE /channels/:channelId/messages/:messageId` | [docs](https://docs.discord.com/developers/resources/message#delete-message) |
| [Delete Own Reaction](actions/delete-own-reaction.md) | `DELETE /channels/:channelId/messages/:messageId/reactions/:emojiName/@me` | [docs](https://docs.discord.com/developers/resources/message#delete-own-reaction) |
| [Edit Message](actions/edit-message.md) | `PATCH /channels/:channelId/messages/:messageId` | [docs](https://docs.discord.com/developers/resources/message#edit-message) |
| [Get Channel](actions/get-channel.md) | `GET /channels/:channelId` | [docs](https://docs.discord.com/developers/resources/channel#get-channel) |
| [Get Channel Message](actions/get-channel-message.md) | `GET /channels/:channelId/messages/:messageId` | [docs](https://docs.discord.com/developers/resources/message#get-channel-message) |
| [Get Current Bot User](actions/get-current-bot-user.md) | `GET /users/@me` | [docs](https://docs.discord.com/developers/resources/user#get-current-user) |
| [Get Guild](actions/get-guild.md) | `GET /guilds/:guildId` | [docs](https://docs.discord.com/developers/resources/guild#get-guild) |
| [Get Guild Member](actions/get-guild-member.md) | `GET /guilds/:guildId/members/:userId` | [docs](https://docs.discord.com/developers/resources/guild#get-guild-member) |
| [Get Reactions](actions/get-reactions.md) | `GET /channels/:channelId/messages/:messageId/reactions/:emojiName` | [docs](https://docs.discord.com/developers/resources/message#get-reactions) |
| [List Channel Messages](actions/list-channel-messages.md) | `GET /channels/:channelId/messages` | [docs](https://docs.discord.com/developers/resources/message#get-channel-messages) |
| [List Guild Channels](actions/list-guild-channels.md) | `GET /guilds/:guildId/channels` | [docs](https://docs.discord.com/developers/resources/guild#get-guild-channels) |
| [List Guild Members](actions/list-guild-members.md) | `GET /guilds/:guildId/members` | [docs](https://docs.discord.com/developers/resources/guild#list-guild-members) |
| [List Guild Roles](actions/list-guild-roles.md) | `GET /guilds/:guildId/roles` | [docs](https://docs.discord.com/developers/resources/guild#get-guild-roles) |
| [Search Guild Members](actions/search-guild-members.md) | `GET /guilds/:guildId/members/search` | [docs](https://docs.discord.com/developers/resources/guild#search-guild-members) |
| [Trigger Typing Indicator](actions/trigger-typing-indicator.md) | `POST /channels/:channelId/typing` | [docs](https://docs.discord.com/developers/resources/channel#trigger-typing-indicator) |
| [Update Channel](actions/update-channel.md) | `PATCH /channels/:channelId` | [docs](https://docs.discord.com/developers/resources/channel#modify-channel) |
