# Insites: Native API Reference

A consolidated summary of Insites's API configuration, with links to official documentation.

- **Official docs:** https://help.insites.com/en/collections/4740612-api-webhooks
- **API base URL:** `https://api.insites.com/api/v1`

## Authentication

### API Key

Authenticate with an Insites server-side API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
api-key: <apiKey>
```

[Official authentication documentation](https://help.insites.com/en/articles/7994893-api-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100). Use `offset` in the query string as the record offset; numbering starts at 0.
