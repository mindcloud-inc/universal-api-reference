# Discord: Native API Reference

A consolidated summary of Discord's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://docs.discord.com/developers/reference
- **API base URL:** `https://discord.com/api/v10`

## Authentication

### OAuth2 (User Token)

Discord OAuth2 user authorization flow (Bearer token). Use for user-scoped endpoints.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://discord.com/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://discord.com/api/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `bot applications.commands identify guilds`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://discord.com/api/oauth2/token.

[Official authentication documentation](https://docs.discord.com/developers/topics/oauth2)

### Bot Token

Use the single API Key field to paste your Discord Bot Token (without the "Bot " prefix). MindCloud sends Authorization: Bot <token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bot <apiKey>
```

[Official authentication documentation](https://docs.discord.com/developers/topics/oauth2#bots)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100). Use `before` in the query string as the pagination cursor.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Delete Messages](actions/bulk-delete-messages.md) | `POST /channels/:channelId/messages/bulk-delete` | [docs](https://docs.discord.com/developers/resources/message#bulk-delete-messages) |
| [Create Guild Ban](actions/create-guild-ban.md) | `PUT /guilds/:guildId/bans/:userId` | [docs](https://docs.discord.com/developers/resources/guild#create-guild-ban) |
| [Create Guild Role](actions/create-guild-role.md) | `POST /guilds/:guildId/roles` | [docs](https://docs.discord.com/developers/resources/guild#create-guild-role) |
| [Create Interaction Response](actions/create-interaction-response.md) | `POST /interactions/:interactionId/:interactionToken/callback` | [docs](https://docs.discord.com/developers/interactions/receiving-and-responding#create-interaction-response) |
| [Create Message](actions/create-message.md) | `POST /channels/:channelId/messages` | [docs](https://docs.discord.com/developers/resources/message#create-message) |
| [Create Reaction](actions/create-reaction.md) | `PUT /channels/:channelId/messages/:messageId/reactions/:emojiName/@me` | [docs](https://docs.discord.com/developers/resources/message#create-reaction) |
| [Delete Guild Role](actions/delete-guild-role.md) | `DELETE /guilds/:guildId/roles/:roleId` | [docs](https://docs.discord.com/developers/resources/guild#delete-guild-role) |
| [Delete Message](actions/delete-message.md) | `DELETE /channels/:channelId/messages/:messageId` | [docs](https://docs.discord.com/developers/resources/message#delete-message) |
| [Delete Own Reaction](actions/delete-own-reaction.md) | `DELETE /channels/:channelId/messages/:messageId/reactions/:emojiName/@me` | [docs](https://docs.discord.com/developers/resources/message#delete-own-reaction) |
| [Get Channel](actions/get-channel.md) | `GET /channels/:channelId` | [docs](https://docs.discord.com/developers/resources/channel#get-channel) |
| [Get Current User](actions/get-current-user.md) | `GET /users/@me` | [docs](https://docs.discord.com/developers/resources/user#get-current-user) |
| [Get Guild Member](actions/get-guild-member.md) | `GET /guilds/:guildId/members/:userId` | [docs](https://docs.discord.com/developers/resources/guild#get-guild-member) |
| [List Current User Guilds](actions/list-current-user-guilds.md) | `GET /users/@me/guilds` | [docs](https://docs.discord.com/developers/resources/user#get-current-user-guilds) |
| [List Guild Channels](actions/list-guild-channels.md) | `GET /guilds/:guildId/channels` | [docs](https://docs.discord.com/developers/resources/guild#get-guild-channels) |
| [List Guild Members](actions/list-guild-members.md) | `GET /guilds/:guildId/members` | [docs](https://docs.discord.com/developers/resources/guild#list-guild-members) |
| [List Guild Roles](actions/list-guild-roles.md) | `GET /guilds/:guildId/roles` | [docs](https://docs.discord.com/developers/resources/guild#get-guild-roles) |
| [List Messages](actions/list-messages.md) | `GET /channels/:channelId/messages` | [docs](https://docs.discord.com/developers/resources/message#get-channel-messages) |
| [Remove Guild Ban](actions/remove-guild-ban.md) | `DELETE /guilds/:guildId/bans/:userId` | [docs](https://docs.discord.com/developers/resources/guild#remove-guild-ban) |
| [Remove Guild Member](actions/remove-guild-member.md) | `DELETE /guilds/:guildId/members/:userId` | [docs](https://docs.discord.com/developers/resources/guild#remove-guild-member) |
| [Trigger Typing Indicator](actions/trigger-typing-indicator.md) | `POST /channels/:channelId/typing` | [docs](https://docs.discord.com/developers/resources/channel#trigger-typing-indicator) |
| [Update Guild Member](actions/update-guild-member.md) | `PATCH /guilds/:guildId/members/:userId` | [docs](https://docs.discord.com/developers/resources/guild#modify-guild-member) |
| [Update Guild Role](actions/update-guild-role.md) | `PATCH /guilds/:guildId/roles/:roleId` | [docs](https://docs.discord.com/developers/resources/guild#modify-guild-role) |
| [Update Message](actions/update-message.md) | `PATCH /channels/:channelId/messages/:messageId` | [docs](https://docs.discord.com/developers/resources/message#edit-message) |
