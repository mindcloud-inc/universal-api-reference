# Peekalink: Native API Reference

A consolidated summary of Peekalink's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://docs.peekalink.io/quickstart
- **API base URL:** `https://api.peekalink.io`

## Authentication

### API Key

Authenticate Peekalink requests with a bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.peekalink.io/quickstart)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get a Link Preview](actions/get-link-preview.md) | `POST /` | [docs](https://docs.peekalink.io/api-reference/link-preview/get-a-link-preview) |
