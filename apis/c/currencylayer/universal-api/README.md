# <img src="https://images.mindcloud.co/apps/icons/currencylayer_1776961100768.png" alt="Currencylayer logo" width="28" height="28"> Currencylayer: Universal API

Get live, historical, and converted currency exchange rates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/currencylayer/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://currencylayer.com/
- **Vendor API docs:** https://marketplace.apilayer.com/currency_data-api/tabs/api_docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Supported Currencies](actions/list-supported-currencies.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/currencylayer/latest/actions/list-supported-currencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Conversion

| Action | Method | Description |
| --- | --- | --- |
| [Convert Currency Amount](actions/convert-currency-amount.md) | GET | Converts a currency amount using Currencylayer rates. |
| [Convert Currency Amount Using Historical Rates](actions/convert-currency-amount-using-historical-rates.md) | GET | Converts a currency amount using historical Currencylayer rates. |

### Currency

| Action | Method | Description |
| --- | --- | --- |
| [List Supported Currencies](actions/list-supported-currencies.md) | GET | Retrieves supported currencies from Currencylayer. |

### Exchangerate

| Action | Method | Description |
| --- | --- | --- |
| [Get Historical Exchange Rates](actions/get-historical-exchange-rates.md) | GET | Retrieves historical exchange rates from Currencylayer for a specific date. |
| [Get Historical Exchange Rates By Source Currency](actions/get-historical-exchange-rates-by-source-currency.md) | GET | Retrieves historical exchange rates by source currency from Currencylayer on a date. |
| [Get Historical Exchange Rates By Source Currency And Selected Currencies](actions/get-historical-exchange-rates-by-source-currency-and-selected-currencies.md) | GET | Retrieves historical exchange rates by source and selected currencies from Currencylayer on a date. |
| [Get Historical Exchange Rates For Selected Currencies](actions/get-historical-exchange-rates-for-selected-currencies.md) | GET | Retrieves historical exchange rates for selected currencies from Currencylayer on a date. |
| [Get Latest Exchange Rates](actions/get-latest-exchange-rates.md) | GET | Retrieves latest exchange rates from Currencylayer. |
| [Get Latest Exchange Rates By Source Currency](actions/get-latest-exchange-rates-by-source-currency.md) | GET | Retrieves latest exchange rates by source currency from Currencylayer. |
| [Get Latest Exchange Rates By Source Currency And Selected Currencies](actions/get-latest-exchange-rates-by-source-currency-and-selected-currencies.md) | GET | Retrieves latest exchange rates by source and selected currencies from Currencylayer. |
| [Get Latest Exchange Rates For Selected Currencies](actions/get-latest-exchange-rates-for-selected-currencies.md) | GET | Retrieves latest exchange rates for selected currencies from Currencylayer. |
| [Get Timeframe Exchange Rates](actions/get-timeframe-exchange-rates.md) | GET | Retrieves exchange rates over a date range from Currencylayer. |
| [Get Timeframe Exchange Rates By Source Currency](actions/get-timeframe-exchange-rates-by-source-currency.md) | GET | Retrieves timeframe exchange rates by source currency from Currencylayer. |
| [Get Timeframe Exchange Rates For Selected Currencies](actions/get-timeframe-exchange-rates-for-selected-currencies.md) | GET | Retrieves timeframe exchange rates for selected currencies from Currencylayer. |

### Exchangeratechange

| Action | Method | Description |
| --- | --- | --- |
| [Get Currency Change](actions/get-currency-change.md) | GET | Retrieves currency change data from Currencylayer. |
| [Get Currency Change Over Timeframe](actions/get-currency-change-over-timeframe.md) | GET | Retrieves currency change data over a timeframe from Currencylayer. |

