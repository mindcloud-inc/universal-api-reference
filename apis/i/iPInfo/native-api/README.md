# IPInfo: Native API Reference

A consolidated summary of IPInfo's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://ipinfo.io/developers
- **OpenAPI specification:** https://ipinfo.io/developers/openapi.yaml
- **API base URL:** `https://api.ipinfo.io`

## Authentication

### API Key

Use an IPInfo access token to call the IPInfo API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://ipinfo.io/developers/)

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Lite IP Lookups](actions/batch-lite-ip-lookups.md) | `POST /batch/lite` | [docs](https://ipinfo.io/developers/advanced-usage) |
| [Create IP Map](actions/create-ip-map.md) | `POST /tools/map` | [docs](https://ipinfo.io/tools/map) |
| [Get Lite IP Details](actions/get-lite-ip-details.md) | `GET /lite/:ip` | [docs](https://ipinfo.io/developers/lite-api) |
| [Get Lite IP Field](actions/get-lite-ip-field.md) | `GET /lite/:ip/:field` | [docs](https://ipinfo.io/developers/lite-api) |
| [Get Lite My IP Details](actions/get-lite-my-ip-details.md) | `GET /lite/me` | [docs](https://ipinfo.io/developers/lite-api) |
| [Get Lite My IP Field](actions/get-lite-my-ip-field.md) | `GET /lite/me/:field` | [docs](https://ipinfo.io/developers/lite-api) |
