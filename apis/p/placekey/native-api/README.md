# Placekey: Native API Reference

A consolidated summary of Placekey's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://docs.placekey.io/documentation
- **API base URL:** `https://api.placekey.io`

## Authentication

### API Key

Authenticate Placekey API requests with an API key generated in the Placekey developer portal.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.placekey.io/documentation/api-overview/authentication)

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

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Placekey](actions/get-placekey.md) | `POST /v1/placekey` | [docs](https://docs.placekey.io/documentation/placekey-api/quick-start) |
| [Get Placekeys](actions/get-placekeys.md) | `POST /v1/placekeys` | [docs](https://docs.placekey.io/documentation/placekey-api/bulk-api) |
