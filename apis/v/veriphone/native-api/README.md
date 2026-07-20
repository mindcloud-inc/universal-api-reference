# Veriphone: Native API Reference

A consolidated summary of Veriphone's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://veriphone.io/docs/v2
- **API base URL:** `https://api.veriphone.io`

## Authentication

### Veriphone API Key

Authenticate with a Veriphone API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://veriphone.io/docs/v2)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Example Phone Number](actions/get-example-phone-number.md) | `GET /v2/example` | [docs](https://veriphone.io/docs/v2) |
| [Validate Phone Number](actions/validate-phone-number.md) | `GET /v2/verify` | [docs](https://veriphone.io/docs/v2) |
