# Kalent: Native API Reference

A consolidated summary of Kalent's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://docs.kalent.ai/introduction
- **API base URL:** `https://app.kalent.ai/api`

## Authentication

### API Key

Send the Kalent API key in the x-api-key header exactly as required by the provider.

### Credentials

- **API Key:** `apiKey` · required · Your Kalent API key from the Kalent developer console.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.kalent.ai/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data.talents`.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Search Talents](actions/search-talents.md) | `POST /v1/search/talents` | [docs](https://docs.kalent.ai/api-reference/search-talents) |
