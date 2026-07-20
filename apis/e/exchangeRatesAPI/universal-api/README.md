# <img src="https://images.mindcloud.co/apps/icons/exchange-rates-api_1776795996375.png" alt="Exchange Rates API logo" width="28" height="28"> Exchange Rates API: Universal API

Exchange Rates API provides current, historical, conversion, time-series, fluctuation, and supported-currency exchange-rate data for more than 170 currencies.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/exchangeRatesAPI/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://exchangeratesapi.io
- **Vendor API docs:** https://exchangeratesapi.io/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Latest Rates](actions/get-latest-rates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exchangeRatesAPI/latest/actions/get-latest-rates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Currency Conversion

| Action | Method | Description |
| --- | --- | --- |
| [Convert Currency](actions/convert-currency.md) | GET | Converts an amount between currencies in Exchange Rates API. |

### Exchange Rate

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest Rates](actions/get-latest-rates.md) | GET | Retrieves latest exchange rates from Exchange Rates API. |

### Exchange Rate Fluctuation

| Action | Method | Description |
| --- | --- | --- |
| [Get Rate Fluctuations](actions/get-rate-fluctuations.md) | GET | Retrieves exchange-rate fluctuations from Exchange Rates API. |

### Historical Exchange Rate

| Action | Method | Description |
| --- | --- | --- |
| [Get Historical Rates](actions/get-historical-rates.md) | GET | Retrieves historical exchange rates from Exchange Rates API. |

### Supported Symbol

| Action | Method | Description |
| --- | --- | --- |
| [List Supported Symbols](actions/list-supported-symbols.md) | GET | Retrieves supported currency symbols from Exchange Rates API. |

### Time Series Exchange Rate

| Action | Method | Description |
| --- | --- | --- |
| [List Time Series Rates](actions/list-time-series-rates.md) | GET | Retrieves time-series exchange rates from Exchange Rates API. |

