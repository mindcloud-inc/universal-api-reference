# LightwaveRF Events: Native API Reference

A consolidated summary of LightwaveRF Events's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://support.lightwaverf.com/knowledge/link-plus-smart-series-api
- **API base URL:** `https://publicapi.lightwaverf.com/v1/`

## Authentication

### Lightwave bearer token

Use a Lightwave Smart Series access token. Runtime requests send it as an Authorization bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://shop.lightwaverf.com/blogs/news/smart-series-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Events](actions/list-events.md) | `GET events` | [docs](https://support.lightwaverf.com/knowledge/link-plus-smart-series-api) |
