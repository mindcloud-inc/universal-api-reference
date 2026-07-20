# URL to Text: Native API Reference

A consolidated summary of URL to Text's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://urltotext.com/documentation/api-docs/url-to-text/
- **API base URL:** `https://urltotext.com/api/v1`

## Authentication

### API Token

URLtoText API token authentication.

### Credentials

- **API Token:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://urltotext.com/documentation/api-docs/url-to-text/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Convert URL to Text](actions/convert-url-to-text.md) | `POST /urltotext/` | [docs](https://urltotext.com/documentation/api-docs/url-to-text/) |
