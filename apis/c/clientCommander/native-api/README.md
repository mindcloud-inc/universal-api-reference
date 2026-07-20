# Client Commander: Native API Reference

A consolidated summary of Client Commander's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://docs.clientcommander.com/api-reference/introduction
- **OpenAPI specification:** https://docs.clientcommander.com/openapi.json
- **API base URL:** `https://api.clientcommander.com/v1`

## Authentication

### API Key

Authenticate with a Client Commander API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.clientcommander.com/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://docs.clientcommander.com/api-reference/users/me) |
