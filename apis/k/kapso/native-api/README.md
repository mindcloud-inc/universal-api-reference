# Kapso: Native API Reference

A consolidated summary of Kapso's API configuration, with links to official documentation.

- **Official docs:** https://docs.kapso.ai/llms.txt
- **API base URL:** `https://api.kapso.ai/platform/v1`

## Authentication

### Kapso API Key

Project API key for Kapso Platform API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://docs.kapso.ai/api/platform/v1/platform-api-overview.md)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `per_page` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.
