# VatcheckAPI: Native API Reference

A consolidated summary of VatcheckAPI's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://vatcheckapi.com/docs
- **API base URL:** `https://api.vatcheckapi.com`

## Authentication

### API Key

Authenticate VatcheckAPI requests with an API key from the VatcheckAPI developer portal.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
apikey: <apiKey>
```

[Official authentication documentation](https://vatcheckapi.com/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,503`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Status](actions/check-status.md) | `GET /v2/status` | [docs](https://vatcheckapi.com/docs/status.html) |
| [Validate VAT Number](actions/validate-vat-number.md) | `GET /v2/check` | [docs](https://vatcheckapi.com/docs/check.html) |
