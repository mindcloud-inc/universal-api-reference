# MoonClerk: Native API Reference

A consolidated summary of MoonClerk's API configuration, with links to official documentation.

- **Official docs:** https://github.com/moonclerk/developer/blob/main/api/README.md
- **API base URL:** `https://api.moonclerk.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://github.com/moonclerk/developer/blob/main/api/README.md)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.moonclerk+json;version=1` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `payments`.

## Pagination

Use `count` in the query string to set the page size (default 10; accepted range 1–100). Use `offset` in the query string as the record offset.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.
