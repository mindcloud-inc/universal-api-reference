# Exchange Rates API: Native API Reference

A consolidated summary of Exchange Rates API's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://exchangeratesapi.io/documentation
- **API base URL:** `https://api.exchangeratesapi.io/v1`

## Authentication

### API Key

Authenticate with an Exchange Rates API access key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://exchangeratesapi.io/documentation/)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Convert Currency](actions/convert-currency.md) | `GET convert` | [docs](https://exchangeratesapi.io/documentation/#convert-endpoint) |
| [Get Historical Rates](actions/get-historical-rates.md) | `GET :date` | [docs](https://exchangeratesapi.io/documentation/#historical-rates-endpoint) |
| [Get Latest Rates](actions/get-latest-rates.md) | `GET latest` | [docs](https://exchangeratesapi.io/documentation/#latest-rates-endpoint) |
| [Get Rate Fluctuations](actions/get-rate-fluctuations.md) | `GET fluctuation` | [docs](https://exchangeratesapi.io/documentation/#fluctuation-endpoint) |
| [List Supported Symbols](actions/list-supported-symbols.md) | `GET symbols` | [docs](https://exchangeratesapi.io/documentation/#supported-symbols-endpoint) |
| [List Time Series Rates](actions/list-time-series-rates.md) | `GET timeseries` | [docs](https://exchangeratesapi.io/documentation/#time-series-endpoint) |
