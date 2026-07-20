# Keygen: Native API Reference

A consolidated summary of Keygen's API configuration, with links to official documentation.

- **Official docs:** https://keygen.sh/docs/api/
- **API base URL:** `https://api.keygen.sh/v1/accounts/:account`

## Authentication

### Bearer Token

Use a Keygen environment or product token with Authorization: Bearer <token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://keygen.sh/docs/api/authentication/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.api+json` |
| `Content-Type` | `application/vnd.api+json` |

Shared parameters:

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account` | path | `string` | yes |

Responses from this API use JSON.

## Pagination

Use `page[size]` in the query string to set the page size (default 25; accepted range 1–100). Use `page[number]` in the query string to choose the page; numbering starts at 1.
