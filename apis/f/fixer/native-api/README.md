# Fixer: Native API Reference

A consolidated summary of Fixer's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://fixer.io/documentation
- **API base URL:** `https://data.fixer.io/api`

## Authentication

### API Key

Use the API key from your Fixer dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://fixer.io/documentation)

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Convert Amount](actions/convert-amount.md) | `GET /convert` | [docs](https://fixer.io/documentation) |
| [Get Fluctuation Rates](actions/get-fluctuation-rates.md) | `GET /fluctuation` | [docs](https://fixer.io/documentation) |
| [Get Historical Exchange Rates](actions/get-historical-exchange-rates.md) | `GET /:date` | [docs](https://fixer.io/documentation) |
| [Get Latest Exchange Rates](actions/get-latest-exchange-rates.md) | `GET /latest` | [docs](https://fixer.io/documentation) |
| [Get Time Series Rates](actions/get-time-series-rates.md) | `GET /timeseries` | [docs](https://fixer.io/documentation) |
| [List Supported Symbols](actions/list-supported-symbols.md) | `GET /symbols` | [docs](https://fixer.io/documentation) |
