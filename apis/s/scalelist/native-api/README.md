# Scalelist: Native API Reference

A consolidated summary of Scalelist's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://app.scalelist.com/docs
- **API base URL:** `https://app.scalelist.com`

## Authentication

### API Key

Use a Scalelist API key from the API key page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.scalelist.com/app/api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Find Email](actions/find-email.md) | `GET /api/ext/finder/email` | [docs](https://app.scalelist.com/docs) |
| [Find Phone](actions/find-phone.md) | `GET /api/ext/finder/phone` | [docs](https://app.scalelist.com/docs) |
