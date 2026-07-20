# CoinCap: Native API Reference

A consolidated summary of CoinCap's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://pro.coincap.io/api-docs/
- **OpenAPI specification:** https://rest.coincap.io/api-docs.json
- **API base URL:** `https://rest.coincap.io/v3`

## Authentication

### API Key

CoinCap API 3.0 uses bearer authentication on the documented REST surface at rest.coincap.io/v3. Provide your CoinCap Pro API key and the app will send it as an Authorization bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://pro.coincap.io/api-docs/)

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–2000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Asset](actions/get-asset.md) | `GET /assets/:slug` | [docs](https://pro.coincap.io/api-docs/) |
| [Get Asset History](actions/get-asset-history.md) | `GET /assets/:slug/history` | [docs](https://pro.coincap.io/api-docs/) |
| [Get Asset Market Cap History](actions/get-asset-market-cap-history.md) | `GET /assets/:slug/marketcap-history` | [docs](https://pro.coincap.io/api-docs/) |
| [Get Asset Markets](actions/get-asset-markets.md) | `GET /assets/:slug/markets` | [docs](https://pro.coincap.io/api-docs/) |
| [Get Exchange](actions/get-exchange.md) | `GET /exchanges/:exchange` | [docs](https://pro.coincap.io/api-docs/) |
| [Get Rate](actions/get-rate.md) | `GET /rates/:slug` | [docs](https://pro.coincap.io/api-docs/) |
| [List Assets](actions/list-assets.md) | `GET /assets` | [docs](https://pro.coincap.io/api-docs/) |
| [List Exchanges](actions/list-exchanges.md) | `GET /exchanges` | [docs](https://pro.coincap.io/api-docs/) |
| [List Markets](actions/list-markets.md) | `GET /markets` | [docs](https://pro.coincap.io/api-docs/) |
| [List Rates](actions/list-rates.md) | `GET /rates` | [docs](https://pro.coincap.io/api-docs/) |
