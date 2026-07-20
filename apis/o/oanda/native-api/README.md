# Oanda: Native API Reference

A consolidated summary of Oanda's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://exchange-rates-api.oanda.com/
- **API base URL:** `https://exchange-rates-api.oanda.com`

## Authentication

### API Key

Connect OANDA Exchange Rates API with your FXDS API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://exchange-rates-api.oanda.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Aggregated Rates](actions/get-aggregated-rates.md) | `GET /v2/rates/aggregated.:ext` | [docs](https://exchange-rates-api.oanda.com/) |
| [Get Candle Rate](actions/get-candle-rate.md) | `GET /v2/rates/candle.:ext` | [docs](https://exchange-rates-api.oanda.com/) |
| [Get Candle Series](actions/get-candle-series.md) | `GET /v2/rates/candles.:ext` | [docs](https://exchange-rates-api.oanda.com/) |
| [Get Dataset](actions/get-dataset.md) | `GET /v2/datasets/:data_set.:ext` | [docs](https://exchange-rates-api.oanda.com/) |
| [Get Forward Rate](actions/get-forward-rate.md) | `GET /v2/rates/forward.:ext` | [docs](https://exchange-rates-api.oanda.com/) |
| [Get Order Book](actions/get-order-book.md) | `GET /v3/instruments/:instrument/orderBook` | [docs](https://exchange-rates-api.oanda.com/) |
| [Get Position Book](actions/get-position-book.md) | `GET /v3/instruments/:instrument/positionBook` | [docs](https://exchange-rates-api.oanda.com/) |
| [Get Rates](actions/get-rates.md) | `GET /v1/rates/:base.:ext` | [docs](https://exchange-rates-api.oanda.com/) |
| [Get Remaining Quotes](actions/get-remaining-quotes.md) | `GET /v2/remaining_quotes.:ext` | [docs](https://exchange-rates-api.oanda.com/) |
| [Get Spot Rates](actions/get-spot-rates.md) | `GET /v2/rates/spot.:ext` | [docs](https://exchange-rates-api.oanda.com/) |
| [Get Supported Forwards](actions/get-supported-forwards.md) | `GET /v2/supported_forwards.:ext` | [docs](https://exchange-rates-api.oanda.com/) |
| [List Currencies](actions/list-currencies.md) | `GET /v2/currencies.:ext` | [docs](https://exchange-rates-api.oanda.com/) |
| [Stream Rates](actions/stream-rates.md) | `GET /v2/rates/stream.:ext` | [docs](https://exchange-rates-api.oanda.com/) |
