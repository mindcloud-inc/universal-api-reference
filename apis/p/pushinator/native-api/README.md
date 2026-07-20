# Pushinator: Native API Reference

A consolidated summary of Pushinator's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://pushinator.com/api
- **API base URL:** `https://api.pushinator.com/api/v2`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://pushinator.com/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | `GET /user` |  |
| [List Channels](actions/list-channels.md) | `GET /channels` |  |
| [Send Notification](actions/send-notification.md) | `POST /notifications/send` | [docs](https://pushinator.com/api#send-notification) |
