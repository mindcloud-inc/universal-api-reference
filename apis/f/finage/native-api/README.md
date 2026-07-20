# Finage: Native API Reference

A consolidated summary of Finage's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://finage.co.uk/docs/api
- **API base URL:** `https://api.finage.co.uk`

## Authentication

### API Key

Use a Finage API key for all requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://finage.co.uk/docs/api)

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Market Status](actions/get-market-status.md) | `GET /marketstatus` | [docs](https://finage.co.uk/docs/api/fundamentals/market-status-api) |
