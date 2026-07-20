# Dashly: Native API Reference

A consolidated summary of Dashly's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://developers.dashly.io/webapi/
- **API base URL:** `https://api.dashly.app`

## Authentication

### API Key

Use Dashly admin-panel auth token from Settings -> Developers -> API Keys.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.dashly.io/webapi/auth/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `paginate_count` in the query string to set the page size (default 20; accepted range 1–50). Use `paginate_position` in the query string as the pagination cursor.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Conversation Tag](actions/add-conversation-tag.md) | `POST conversations/:id/tag` | [docs](https://developers.dashly.io/webapi/endpoints/conversations/tag/post/) |
| [Assign Conversation](actions/assign-conversation.md) | `POST conversations/:id/assign` | [docs](https://developers.dashly.io/webapi/endpoints/conversations/assign/) |
| [Close Conversation](actions/close-conversation.md) | `POST conversations/:id/close` | [docs](https://developers.dashly.io/webapi/endpoints/conversations/close/) |
| [Get Conversation](actions/get-conversation.md) | `GET conversations/:id` | [docs](https://developers.dashly.io/webapi/endpoints/conversations/conversation/) |
| [Get Conversation Parts](actions/get-conversation-parts.md) | `GET conversations/:id/parts` | [docs](https://developers.dashly.io/webapi/endpoints/conversations/parts/) |
| [Get User](actions/get-user.md) | `GET users/:id` | [docs](https://developers.dashly.io/webapi/endpoints/users/user/) |
| [Import User Properties from CSV](actions/import-user-properties-from-csv.md) | `POST users/import` | [docs](https://developers.dashly.io/webapi/endpoints/users/import/) |
| [List Active Users](actions/list-active-users.md) | `GET apps/:id/activeusers` | [docs](https://developers.dashly.io/webapi/endpoints/apps/activeusers/) |
| [List App Conversations](actions/list-app-conversations.md) | `GET apps/:id/conversations` | [docs](https://developers.dashly.io/webapi/endpoints/apps/conversations/) |
| [List Channels](actions/list-channels.md) | `GET apps/:id/channels` | [docs](https://developers.dashly.io/webapi/endpoints/apps/channels/) |
| [List User Conversations](actions/list-user-conversations.md) | `GET users/:id/conversations` | [docs](https://developers.dashly.io/webapi/endpoints/users/conversations/) |
| [List User Events](actions/list-user-events.md) | `GET users/:id/events` | [docs](https://developers.dashly.io/webapi/endpoints/users/events/get/) |
| [List Users](actions/list-users.md) | `GET apps/:id/users` | [docs](https://developers.dashly.io/webapi/endpoints/apps/users/) |
| [Remove Conversation Tag](actions/remove-conversation-tag.md) | `DELETE conversations/:id/tag` | [docs](https://developers.dashly.io/webapi/endpoints/conversations/tag/delete/) |
| [Reply In Conversation](actions/reply-in-conversation.md) | `POST conversations/:id/reply` | [docs](https://developers.dashly.io/webapi/endpoints/conversations/reply/) |
| [Send Manual Message To User](actions/send-manual-message-to-user.md) | `POST users/:id/sendmessage` | [docs](https://developers.dashly.io/webapi/endpoints/users/sendmessage/) |
| [Set Conversation Typing Indicator](actions/set-conversation-typing-indicator.md) | `POST conversations/:id/settyping` | [docs](https://developers.dashly.io/webapi/endpoints/conversations/settyping/) |
| [Set User Presence](actions/set-user-presence.md) | `POST users/:id/setpresence` | [docs](https://developers.dashly.io/webapi/endpoints/users/setpresence/) |
| [Set User Properties](actions/set-user-properties.md) | `POST users/:id/props` | [docs](https://developers.dashly.io/webapi/endpoints/users/props/) |
| [Start Conversation For User](actions/start-conversation-for-user.md) | `POST users/:id/startconversation` | [docs](https://developers.dashly.io/webapi/endpoints/users/startconversation/) |
| [Track User Event](actions/track-user-event.md) | `POST users/:id/events` | [docs](https://developers.dashly.io/webapi/endpoints/users/events/post/) |
