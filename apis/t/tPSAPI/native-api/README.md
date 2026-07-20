# TPS API: Native API Reference

A consolidated summary of TPS API's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://tpsapi.com/docs
- **API base URL:** `https://service.tpsapi.com`

## Authentication

### API Key

Use the authorization token from your TPS API account page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://tpsapi.com/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Screen Phone Numbers](actions/screen-phone-numbers.md) | `POST /` | [docs](https://tpsapi.com/docs) |
