# Microsoft Teams: Native API Reference

A consolidated summary of Microsoft Teams's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/graph/api/resources/teams-api-overview?view=graph-rest-1.0
- **API base URL:** `https://graph.microsoft.com`

## Authentication

### Microsoft Entra OAuth2

Delegated OAuth2 for Microsoft Teams and Microsoft Graph using a work or school account in a Teams-enabled tenant.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://login.microsoftonline.com/common/oauth2/v2.0/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://login.microsoftonline.com/common/oauth2/v2.0/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `offline_access User.Read Team.ReadBasic.All TeamMember.Read.All Channel.ReadBasic.All ChannelSettings.ReadWrite.All Channel.Create ChannelMember.Read.All Files.Read.All TeamsTab.Read.All TeamsAppInstallation.ReadForTeam ChannelMessage.Read.All ChannelMessage.Send Chat.ReadWrite ChatMessage.Send Chat.Create TeamsAppInstallation.ReadForChat`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://login.microsoftonline.com/common/oauth2/v2.0/token.

[Official authentication documentation](https://learn.microsoft.com/en-us/entra/identity-platform/v2-oauth2-auth-code-flow)

## API conventions

Responses from this API use JSON. Response data is read from `value`.

## Pagination

Use `$top` in the query string to set the page size (default 25; accepted range 1–50). Use `$skiptoken` in the query string as the pagination cursor. Follow the complete next-page URL returned by the API.

## Filtering

Send filters in the query string. Supported operators: `contains`, `eq`, `startsWith`.

## Sorting

Set the sort field with `$orderby` in the query string. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Channel](actions/create-channel.md) | `POST /v1.0/teams/:teamId/channels` | [docs](https://learn.microsoft.com/en-us/graph/api/channel-post?view=graph-rest-1.0) |
| [Create Chat](actions/create-chat.md) | `POST /v1.0/chats` | [docs](https://learn.microsoft.com/en-us/graph/api/chat-post?view=graph-rest-1.0) |
| [Get Channel](actions/get-channel.md) | `GET /v1.0/teams/:teamId/channels/:channelId` | [docs](https://learn.microsoft.com/en-us/graph/api/channel-get?view=graph-rest-1.0) |
| [Get Channel Files Folder](actions/get-channel-files-folder.md) | `GET /v1.0/teams/:teamId/channels/:channelId/filesFolder` | [docs](https://learn.microsoft.com/en-us/graph/api/channel-get-filesfolder?view=graph-rest-1.0) |
| [Get Chat](actions/get-chat.md) | `GET /v1.0/chats/:chatId` | [docs](https://learn.microsoft.com/en-us/graph/api/chat-get?view=graph-rest-1.0) |
| [Get Team](actions/get-team.md) | `GET /v1.0/teams/:teamId` | [docs](https://learn.microsoft.com/en-us/graph/api/team-get?view=graph-rest-1.0) |
| [Get Team Primary Channel](actions/get-team-primary-channel.md) | `GET /v1.0/teams/:teamId/primaryChannel` | [docs](https://learn.microsoft.com/en-us/graph/api/team-get-primarychannel?view=graph-rest-1.0) |
| [List All Team Channels](actions/list-all-team-channels.md) | `GET /v1.0/teams/:teamId/allChannels` | [docs](https://learn.microsoft.com/en-us/graph/api/channel-list-allchannels?view=graph-rest-1.0) |
| [List Channel Members](actions/list-channel-members.md) | `GET /v1.0/teams/:teamId/channels/:channelId/members` | [docs](https://learn.microsoft.com/en-us/graph/api/channel-list-members?view=graph-rest-1.0) |
| [List Channel Message Replies](actions/list-channel-message-replies.md) | `GET /v1.0/teams/:teamId/channels/:channelId/messages/:messageId/replies` | [docs](https://learn.microsoft.com/en-us/graph/api/chatmessage-list-replies?view=graph-rest-1.0) |
| [List Channel Messages](actions/list-channel-messages.md) | `GET /v1.0/teams/:teamId/channels/:channelId/messages` | [docs](https://learn.microsoft.com/en-us/graph/api/channel-list-messages?view=graph-rest-1.0) |
| [List Channel Tabs](actions/list-channel-tabs.md) | `GET /v1.0/teams/:teamId/channels/:channelId/tabs` | [docs](https://learn.microsoft.com/en-us/graph/api/channel-list-tabs?view=graph-rest-1.0) |
| [List Chat Members](actions/list-chat-members.md) | `GET /v1.0/chats/:chatId/members` | [docs](https://learn.microsoft.com/en-us/graph/api/chat-list-members?view=graph-rest-1.0) |
| [List Chat Messages](actions/list-chat-messages.md) | `GET /v1.0/chats/:chatId/messages` | [docs](https://learn.microsoft.com/en-us/graph/api/chat-list-messages?view=graph-rest-1.0) |
| [List Chats](actions/list-chats.md) | `GET /v1.0/me/chats` | [docs](https://learn.microsoft.com/en-us/graph/api/chat-list?view=graph-rest-1.0) |
| [List Joined Teams](actions/list-joined-teams.md) | `GET /v1.0/me/joinedTeams` | [docs](https://learn.microsoft.com/en-us/graph/api/user-list-joinedteams?view=graph-rest-1.0) |
| [List Team Channels](actions/list-team-channels.md) | `GET /v1.0/teams/:teamId/channels` | [docs](https://learn.microsoft.com/en-us/graph/api/channel-list?view=graph-rest-1.0) |
| [List Team Installed Apps](actions/list-team-installed-apps.md) | `GET /v1.0/teams/:teamId/installedApps` | [docs](https://learn.microsoft.com/en-us/graph/api/team-list-installedapps?view=graph-rest-1.0) |
| [List Team Members](actions/list-team-members.md) | `GET /v1.0/teams/:teamId/members` | [docs](https://learn.microsoft.com/en-us/graph/api/team-list-members?view=graph-rest-1.0) |
| [Reply To Channel Message](actions/reply-to-channel-message.md) | `POST /v1.0/teams/:teamId/channels/:channelId/messages/:messageId/replies` | [docs](https://learn.microsoft.com/en-us/graph/api/chatmessage-post-replies?view=graph-rest-1.0) |
| [Send Channel Message](actions/send-channel-message.md) | `POST /v1.0/teams/:teamId/channels/:channelId/messages` | [docs](https://learn.microsoft.com/en-us/graph/api/channel-post-messages?view=graph-rest-1.0) |
| [Send Chat Message](actions/send-chat-message.md) | `POST /v1.0/chats/:chatId/messages` | [docs](https://learn.microsoft.com/en-us/graph/api/chat-post-messages?view=graph-rest-1.0) |
| [Update Channel](actions/update-channel.md) | `PATCH /v1.0/teams/:teamId/channels/:channelId` | [docs](https://learn.microsoft.com/en-us/graph/api/channel-patch?view=graph-rest-1.0) |
