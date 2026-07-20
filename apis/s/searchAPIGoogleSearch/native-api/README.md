# SearchAPI - Google Search: Native API Reference

A consolidated summary of SearchAPI - Google Search's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://www.searchapi.io/docs/google
- **API base URL:** `https://www.searchapi.io/api/v1`

## Authentication

### API Key

Authenticate requests to SearchAPI with an API key. SearchAPI accepts the key either as api_key or as an Authorization Bearer token; this app uses the bearer-token form.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.searchapi.io/docs/google)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Find Supported Locations](actions/find-supported-locations.md) | `GET /locations` | [docs](https://www.searchapi.io/docs/locations-api) |
| [Get Account Usage](actions/get-account-usage.md) | `GET /me` | [docs](https://www.searchapi.io/docs/account-api) |
| [Search Google](actions/search-google.md) | `GET /search` | [docs](https://www.searchapi.io/docs/google) |
