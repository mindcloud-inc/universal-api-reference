# Sandbox: Native API Reference

A consolidated summary of Sandbox's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://developer.sandbox.co.in/
- **API base URL:** `https://api.sandbox.co.in`

## Authentication

### Custom

Authenticate with a Sandbox API key and API secret to generate a 24-hour access token.

### Credentials

- **API Key:** `apiKey` · required · Sandbox API key from the Sandbox Console.
- **API Secret:** `apiSecret` · required · Sandbox API secret used only to generate the 24-hour access token.

Send these headers with each API request:

```http
x-api-key: <apiKey>
x-api-secret: <apiSecret>
Authorization: <custom.data.access_token>
```

[Official authentication documentation](https://developer.sandbox.co.in/api-reference/authenticate)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |
| `x-api-version` | `1.0` |

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | `POST /authenticate` | [docs](https://developer.sandbox.co.in/api-reference/authenticate) |
| [Search GSTIN](actions/search-gstin.md) | `POST /gst/compliance/public/gstin/search` | [docs](https://developer.sandbox.co.in/api-reference/gst/compliance/endpoints/public/search_gstin) |
