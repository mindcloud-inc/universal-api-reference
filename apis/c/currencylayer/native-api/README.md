# Currencylayer: Native API Reference

A consolidated summary of Currencylayer's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://marketplace.apilayer.com/currency_data-api/tabs/api_docs
- **API base URL:** `https://api.currencylayer.com`

## Authentication

### API key

Currencylayer uses the legacy query-string auth contract for this draft app: send the implicit `{{credentials.apiKey}}` value as the shared `access_key` query parameter to `https://api.currencylayer.com` endpoints.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://currencylayer.com/documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Convert Currency Amount](actions/convert-currency-amount.md) | `GET /convert` | [docs](https://currencylayer.com/documentation) |
| [Convert Currency Amount Using Historical Rates](actions/convert-currency-amount-using-historical-rates.md) | `GET /convert` | [docs](https://currencylayer.com/documentation) |
| [Get Currency Change](actions/get-currency-change.md) | `GET /change` | [docs](https://currencylayer.com/documentation) |
| [Get Currency Change Over Timeframe](actions/get-currency-change-over-timeframe.md) | `GET /change` | [docs](https://currencylayer.com/documentation) |
| [Get Historical Exchange Rates](actions/get-historical-exchange-rates.md) | `GET /historical` | [docs](https://currencylayer.com/documentation) |
| [Get Historical Exchange Rates By Source Currency](actions/get-historical-exchange-rates-by-source-currency.md) | `GET /historical` | [docs](https://currencylayer.com/documentation) |
| [Get Historical Exchange Rates By Source Currency And Selected Currencies](actions/get-historical-exchange-rates-by-source-currency-and-selected-currencies.md) | `GET /historical` | [docs](https://currencylayer.com/documentation) |
| [Get Historical Exchange Rates For Selected Currencies](actions/get-historical-exchange-rates-for-selected-currencies.md) | `GET /historical` | [docs](https://currencylayer.com/documentation) |
| [Get Latest Exchange Rates](actions/get-latest-exchange-rates.md) | `GET /live` | [docs](https://currencylayer.com/documentation) |
| [Get Latest Exchange Rates By Source Currency](actions/get-latest-exchange-rates-by-source-currency.md) | `GET /live` | [docs](https://currencylayer.com/documentation) |
| [Get Latest Exchange Rates By Source Currency And Selected Currencies](actions/get-latest-exchange-rates-by-source-currency-and-selected-currencies.md) | `GET /live` | [docs](https://currencylayer.com/documentation) |
| [Get Latest Exchange Rates For Selected Currencies](actions/get-latest-exchange-rates-for-selected-currencies.md) | `GET /live` | [docs](https://currencylayer.com/documentation) |
| [Get Timeframe Exchange Rates](actions/get-timeframe-exchange-rates.md) | `GET /timeframe` | [docs](https://currencylayer.com/documentation) |
| [Get Timeframe Exchange Rates By Source Currency](actions/get-timeframe-exchange-rates-by-source-currency.md) | `GET /timeframe` | [docs](https://currencylayer.com/documentation) |
| [Get Timeframe Exchange Rates For Selected Currencies](actions/get-timeframe-exchange-rates-for-selected-currencies.md) | `GET /timeframe` | [docs](https://currencylayer.com/documentation) |
| [List Supported Currencies](actions/list-supported-currencies.md) | `GET /list` | [docs](https://currencylayer.com/documentation) |
