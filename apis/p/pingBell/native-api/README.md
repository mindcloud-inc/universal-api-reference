# PingBell: Native API Reference

A consolidated summary of PingBell's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://pingbell.io/docs/pingbell-api/
- **API base URL:** `https://app.pingbell.io`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://pingbell.io/knowledge-base/account-billing/getting-your-api-key/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List PingBells](actions/list-pingbells.md) | `GET /userPingbells` | [docs](https://pingbell.io/docs/pingbell-api/get-pingbells/) |
| [Send Notification](actions/send-notification.md) | `POST /log` | [docs](https://pingbell.io/docs/pingbell-api/post-notifications/) |
