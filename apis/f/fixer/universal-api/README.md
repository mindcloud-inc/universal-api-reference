# <img src="https://images.mindcloud.co/apps/icons/favicon-fixer-io-48x48_1776260683459.png" alt="Fixer logo" width="28" height="28"> Fixer: Universal API

Get live and historical foreign exchange rates, convert amounts, and inspect currency metadata from Fixer.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fixer/latest
- **Category:** Commerce / Accounting
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://fixer.io
- **Vendor API docs:** https://fixer.io/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Supported Symbols](actions/list-supported-symbols.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fixer/latest/actions/list-supported-symbols?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Currency Symbol

| Action | Method | Description |
| --- | --- | --- |
| [List Supported Symbols](actions/list-supported-symbols.md) | GET | Retrieves supported currency symbols from Fixer. |

### Exchange Rate

| Action | Method | Description |
| --- | --- | --- |
| [Convert Amount](actions/convert-amount.md) | GET | Converts an amount between currencies in Fixer. |
| [Get Historical Exchange Rates](actions/get-historical-exchange-rates.md) | GET | Retrieves historical exchange rates from Fixer by date. |
| [Get Latest Exchange Rates](actions/get-latest-exchange-rates.md) | GET | Retrieves latest exchange rates from Fixer. |
| [Get Time Series Rates](actions/get-time-series-rates.md) | GET | Retrieves time-series exchange rates from Fixer. |

### Exchange Rate Fluctuation

| Action | Method | Description |
| --- | --- | --- |
| [Get Fluctuation Rates](actions/get-fluctuation-rates.md) | GET | Retrieves exchange rate fluctuations from Fixer. |

