# ReviewStream: Native API Reference

A consolidated summary of ReviewStream's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://support.reviewstream.ai/api/
- **API base URL:** `https://api.reviewstream.ai/api`

## Authentication

### Bearer Token

Authenticate ReviewStream API requests with a JWT bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.reviewstream.ai/api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Reviews](actions/list-reviews.md) | `GET /reviews` | [docs](https://support.reviewstream.ai/api/) |
| [List Surveys](actions/list-surveys.md) | `GET /surveys` | [docs](https://support.reviewstream.ai/api/) |
