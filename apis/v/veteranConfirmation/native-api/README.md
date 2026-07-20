# Veteran Confirmation: Native API Reference

A consolidated summary of Veteran Confirmation's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://developer.va.gov/explore/api/veteran-confirmation/docs
- **OpenAPI specification:** https://api.va.gov/internal/docs/veteran-confirmation/v1/openapi.json
- **API base URL:** `https://sandbox-api.va.gov/services/veteran-confirmation/v1`

## Authentication

### API Key

Authenticate requests with a VA API key in the apikey request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
apikey: <apiKey>
```

[Official authentication documentation](https://developer.va.gov/explore/api/veteran-confirmation/docs?version=current)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Confirm Veteran Status](actions/confirm-veteran-status.md) | `POST /status` | [docs](https://developer.va.gov/explore/api/veteran-confirmation/docs?version=current) |
