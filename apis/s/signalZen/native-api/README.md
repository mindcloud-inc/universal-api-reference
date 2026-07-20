# SignalZen: Native API Reference

A consolidated summary of SignalZen's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://docs.signalzen.com/docs/category/api/
- **API base URL:** `https://api.signalzen.com/external`

## Authentication

### API Secret

Use your SignalZen API Secret key for bearer-authenticated backend API access.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.signalzen.com/docs/api/authentication/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.signalzen.v1+json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 5; minimum 1). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get User](actions/get-user.md) | `GET /users/{userId}` | [docs](https://docs.signalzen.com/docs/api/users/#get-a-user) |
| [Get User Message](actions/get-user-message.md) | `GET /users/{userId}/messages/{messageId}` | [docs](https://docs.signalzen.com/docs/api/messages/#get-a-message) |
| [List User Messages](actions/list-user-messages.md) | `GET /users/{userId}/messages` | [docs](https://docs.signalzen.com/docs/api/messages/#get-all-messages-that-belong-to-a-user) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://docs.signalzen.com/docs/api/users/#get-all-users) |
