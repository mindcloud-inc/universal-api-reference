# IP2Proxy: Native API Reference

A consolidated summary of IP2Proxy's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://www.ip2location.com/web-service/ip2proxy
- **API base URL:** `https://api.ip2proxy.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.ip2location.com/web-service/ip2proxy)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Proxy Lookup](actions/get-proxy-lookup.md) | `GET /` | [docs](https://www.ip2location.com/web-service/ip2proxy) |
| [Get Remaining Credits](actions/get-remaining-credits.md) | `GET /` | [docs](https://www.ip2location.com/web-service/ip2proxy) |
