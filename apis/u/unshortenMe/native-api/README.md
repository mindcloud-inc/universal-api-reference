# Unshorten.Me: Native API Reference

A consolidated summary of Unshorten.Me's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://unshorten.me/api
- **API base URL:** `https://unshorten.me`

## Authentication

### API Token

Connect using an Unshorten.Me API token from the user profile page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://unshorten.me/api)

## API conventions

Responses from this API use JSON.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Unshorten URL](actions/unshorten-url.md) | `GET /api/v2/unshorten` | [docs](https://unshorten.me/api) |
