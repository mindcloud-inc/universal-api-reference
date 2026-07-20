# Stream: Native API Reference

A consolidated summary of Stream's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://getstream.io/chat/docs/
- **OpenAPI specification:** https://raw.githubusercontent.com/GetStream/protocol/main/openapi/chat-openapi.yaml
- **API base URL:** `https://chat.stream-io-api.com`

## Authentication

### App Credentials (API Key + Secret)

Use your Stream API key and secret to generate server-side JWT authentication.

### Credentials

- **API Key:** `apiKey` · required
- **Secret:** `secret` · required · Used to sign Stream server-side JWT requests.

[Official authentication documentation](https://getstream.io/chat/docs/javascript/tokens_and_authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Ban User](actions/ban-user.md) | `POST /moderation/ban` | [docs](https://getstream.io/moderation/docs/api/flag-mute-ban/) |
| [Create Poll](actions/create-poll.md) | `POST /polls` | [docs](https://getstream.io/chat/docs/javascript/polls_api/) |
| [Deactivate User](actions/deactivate-user.md) | `POST /users/:user_id/deactivate` | [docs](https://getstream.io/chat/docs/javascript/update_users/) |
| [Delete Message](actions/delete-message.md) | `DELETE /messages/:id` | [docs](https://getstream.io/chat/docs/javascript/send_message/) |
| [Delete Reaction](actions/delete-reaction.md) | `DELETE /messages/:id/reaction/:type` | [docs](https://getstream.io/chat/docs/javascript/send_reaction/) |
| [Get App Settings](actions/get-app-settings.md) | `GET /app` | [docs](https://getstream.io/chat/docs/javascript/app_setting_overview/) |
| [Get Message](actions/get-message.md) | `GET /messages/:id` | [docs](https://getstream.io/chat/docs/javascript/send_message/) |
| [Get Or Create Channel](actions/get-or-create-channel.md) | `POST /channels/:type/:id/query` | [docs](https://getstream.io/chat/docs/javascript/channel_pagination/) |
| [Hide Channel](actions/hide-channel.md) | `POST /channels/:type/:id/hide` | [docs](https://getstream.io/chat/docs/javascript/hiding_channels/) |
| [List Channel Messages](actions/list-channel-messages.md) | `GET /channels/:type/:id/messages` | [docs](https://getstream.io/chat/docs/javascript/channel_pagination/) |
| [List Message Replies](actions/list-message-replies.md) | `GET /messages/:parent_id/replies` | [docs](https://getstream.io/chat/docs/javascript/threads/) |
| [Reactivate User](actions/reactivate-user.md) | `POST /users/:user_id/reactivate` | [docs](https://getstream.io/chat/docs/javascript/update_users/) |
| [Search Channels](actions/search-channels.md) | `POST /channels` | [docs](https://getstream.io/chat/docs/javascript/query_channels/) |
| [Search Messages](actions/search-messages.md) | `GET /search` | [docs](https://getstream.io/chat/docs/javascript/search/) |
| [Search Polls](actions/search-polls.md) | `POST /polls/query` | [docs](https://getstream.io/chat/docs/javascript/polls_api/) |
| [Search Threads](actions/search-threads.md) | `POST /threads` | [docs](https://getstream.io/chat/docs/javascript/threads/) |
| [Send Message](actions/send-message.md) | `POST /channels/:type/:id/message` | [docs](https://getstream.io/chat/docs/javascript/send_message/) |
| [Send Reaction](actions/send-reaction.md) | `POST /messages/:id/reaction` | [docs](https://getstream.io/chat/docs/javascript/send_reaction/) |
| [Send User Event](actions/send-user-event.md) | `POST /users/:user_id/event` | [docs](https://getstream.io/chat/docs/javascript/event_object/) |
| [Show Channel](actions/show-channel.md) | `POST /channels/:type/:id/show` | [docs](https://getstream.io/chat/docs/javascript/hiding_channels/) |
| [Unban User](actions/unban-user.md) | `DELETE /moderation/ban` | [docs](https://getstream.io/moderation/docs/api/flag-mute-ban/) |
| [Update Channel](actions/update-channel.md) | `POST /channels/:type/:id` | [docs](https://getstream.io/chat/docs/javascript/channel_update/) |
| [Update Message](actions/update-message.md) | `PUT /messages/:id` | [docs](https://getstream.io/chat/docs/javascript/send_message/) |
| [Upsert Users](actions/upsert-users.md) | `POST /users` | [docs](https://getstream.io/chat/docs/javascript/update_users/) |
