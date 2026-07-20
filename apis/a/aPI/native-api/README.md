# 44API: Native API Reference

A consolidated summary of 44API's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://docs.44api.dev
- **OpenAPI specification:** https://docs.44api.dev/openapi.yaml
- **API base URL:** `https://api.44api.dev`

## Authentication

### API Key

Use your 44API API key in the X-API-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://docs.44api.dev)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Health Check](actions/health-check.md) | `GET /webhook/core/health` | [docs](https://docs.44api.dev) |
| [Manage IP Whitelist](actions/manage-ip-whitelist.md) | `POST /webhook/ip-whitelist` | [docs](https://docs.44api.dev) |
| [Validate VAT Number](actions/validate-vat-number.md) | `POST /webhook/validate-vat` | [docs](https://docs.44api.dev) |
