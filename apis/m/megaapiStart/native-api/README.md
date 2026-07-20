# Megaapi Start: Native API Reference

A consolidated summary of Megaapi Start's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://doc.mega-api.app.br
- **API base URL:** `https://{host}`

## Authentication

### API Key

Bearer token authentication with tenant host and instance key.

### Credentials

- **API Key:** `apiKey` · required
- **Host:** `host` · required · MegaAPI tenant host shown in the instance details.
- **Instance Key:** `instanceKey` · required · Instance key used in MegaAPI request paths.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://doc.mega-api.app.br/doc-724956)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Connection Status](actions/get-connection-status.md) | `GET /rest/instance/:instance_key` | [docs](https://doc.mega-api.app.br/api-10974901) |
