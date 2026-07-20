# Minerstat: Native API Reference

A consolidated summary of Minerstat's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://api.minerstat.com/
- **API base URL:** `https://api.minerstat.com`

## Authentication

### API Key

Connect with a Minerstat developer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://api.minerstat.com/docs-coins/documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Coins](actions/list-coins.md) | `GET /v2/coins` | [docs](https://api.minerstat.com/docs-coins/documentation) |
| [List Hardware](actions/list-hardware.md) | `GET /v2/hardware` | [docs](https://api.minerstat.com/docs-hardware/documentation) |
| [List Pools](actions/list-pools.md) | `GET /v2/pools` | [docs](https://api.minerstat.com/docs-pools/documentation) |
