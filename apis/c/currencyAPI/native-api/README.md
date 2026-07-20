# CurrencyAPI: Native API Reference

A consolidated summary of CurrencyAPI's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://currencyapi.com/docs
- **API base URL:** `https://api.currencyapi.com`

## Authentication

### API Key

Use an API key from your CurrencyAPI dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
apikey: <apiKey>
```

[Official authentication documentation](https://currencyapi.com/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get API Status](actions/get-api-status.md) | `GET /v3/status` | [docs](https://currencyapi.com/docs/status) |
| [Get Historical Exchange Rates](actions/get-historical-exchange-rates.md) | `GET /v3/historical` | [docs](https://currencyapi.com/docs/historical) |
| [Get Latest Exchange Rates](actions/get-latest-exchange-rates.md) | `GET /v3/latest` | [docs](https://currencyapi.com/docs/latest) |
| [List Currencies](actions/list-currencies.md) | `GET /v3/currencies` | [docs](https://currencyapi.com/docs/currencies) |
