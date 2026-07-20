# IP2Location IO: Native API Reference

A consolidated summary of IP2Location IO's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.ip2location.io/ip2location-documentation
- **OpenAPI specification:** https://raw.githubusercontent.com/ip2location-com/ip2location-io-openapi/main/json/IPGeolocation.json
- **API base URL:** `https://api.ip2location.io`

## Authentication

### API Key

Authenticate with your IP2Location.io API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.ip2location.io/ip2location-documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get IP Geolocation](actions/get-ip-geolocation.md) | `GET /` | [docs](https://www.ip2location.io/ip2location-documentation) |
