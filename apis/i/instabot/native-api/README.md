# Instabot: Native API Reference

A consolidated summary of Instabot's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://docs.instabot.io/docs/serverapi
- **API base URL:** `https://api.instabot.io/v1`

## Authentication

### API Key

Use your Instabot API Key and Master API Key.

### Credentials

- **API Key:** `apiKey` · required
- **Master API Key:** `masterApiKey` · required · Instabot Master API Key used in the Authorization header.

Send these headers with each API request:

```http
X-Instabot-Api-Key: <apiKey>
```

[Official authentication documentation](https://docs.instabot.io/docs/serverapi)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size. Use `skip` in the query string as the record offset; numbering starts at 0.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://docs.instabot.io/docs/serverapi-users) |
| [Delete User](actions/delete-user.md) | `DELETE /users/:id` | [docs](https://docs.instabot.io/docs/serverapi-users) |
| [Get Application Info](actions/get-application-info.md) | `GET /` | [docs](https://docs.instabot.io/docs/serverapi) |
| [Get Bot Common Summary Of Reply](actions/get-bot-common-summary-of-reply.md) | `GET /instabot/bots/:id/commonSummaryOfReply` | [docs](https://docs.instabot.io/reference/get_instabot-bots-id-commonsummaryofreply) |
| [Get Bot Itemized Summary Of Reply](actions/get-bot-itemized-summary-of-reply.md) | `GET /instabot/bots/:id/itemizedSummaryOfReply` | [docs](https://docs.instabot.io/reference/get_instabot-bots-id-itemizedsummaryofreply) |
| [Get Display Settings](actions/get-display-settings.md) | `GET /instabot/displaySettings` | [docs](https://docs.instabot.io/reference/get_instabot-displaysettings) |
| [Get Live Chat Status Counts](actions/get-live-chat-status-counts.md) | `POST /instabot/chats/liveChatStatusCounts` | [docs](https://docs.instabot.io/reference/post_instabot-chats-livechatstatuscounts) |
| [Get User](actions/get-user.md) | `GET /users/:id` | [docs](https://docs.instabot.io/docs/serverapi-users) |
| [List Bots](actions/list-bots.md) | `GET /instabot/admin/bots` | [docs](https://docs.instabot.io/reference/get_instabot-admin-bots) |
| [List Conversations](actions/list-conversations.md) | `GET /instabot/conversations` | [docs](https://docs.instabot.io/reference/get_instabot-conversations) |
| [List Message Templates](actions/list-message-templates.md) | `GET /instabot/messageTemplates` | [docs](https://docs.instabot.io/reference/get_instabot-messagetemplates) |
| [List Recently Updated Users](actions/list-recently-updated-users.md) | `GET /users/lastUpdated` | [docs](https://docs.instabot.io/docs/serverapi-users) |
| [List Templates](actions/list-templates.md) | `GET /instabot/templates` | [docs](https://docs.instabot.io/reference/get_instabot-templates) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://docs.instabot.io/docs/serverapi-users) |
| [Restore User](actions/restore-user.md) | `POST /users/:id` | [docs](https://docs.instabot.io/docs/serverapi-users) |
| [Search Chats](actions/search-chats.md) | `POST /instabot/chats/search` | [docs](https://docs.instabot.io/reference/post_instabot-chats-search) |
| [Update User](actions/update-user.md) | `PUT /users/:id` | [docs](https://docs.instabot.io/docs/serverapi-users) |
