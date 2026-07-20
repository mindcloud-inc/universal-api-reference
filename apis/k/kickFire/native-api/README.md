# KickFire: Native API Reference

A consolidated summary of KickFire's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://foundryco.com/developers/
- **API base URL:** `https://api.kickfire.com`

## Authentication

### API Key

Use a KickFire API key for a company access point.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.kickfire.com/api/api-getting-started)

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get API Usage](actions/get-api-usage.md) | `GET /usage` | [docs](https://foundryco.com/developers/#api-usage) |
| [Get Company by IP Address](actions/get-company-by-ip-address.md) | `GET /v3/company` | [docs](https://foundryco.com/developers/#ip-to-company-endpoint) |
| [Get Company by Website](actions/get-company-by-website.md) | `GET /v3/company` | [docs](https://foundryco.com/developers/#ip-to-company-endpoint) |
| [Get My API Data](actions/get-my-api-data.md) | `GET /my` | [docs](https://foundryco.com/developers/#myapi) |
