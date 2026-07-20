# <img src="https://images.mindcloud.co/apps/icons/currency-api_1774284877819.png" alt="CurrencyAPI logo" width="28" height="28"> CurrencyAPI: Universal API

Get exchange rates, convert amounts, and inspect currency metadata

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/currencyAPI/latest
- **Category:** Commerce / Accounting
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://currencyapi.com
- **Vendor API docs:** https://currencyapi.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get API Status](actions/get-api-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/currencyAPI/latest/actions/get-api-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Currency

| Action | Method | Description |
| --- | --- | --- |
| [List Currencies](actions/list-currencies.md) | GET | Retrieves supported currency definitions from CurrencyAPI. |

### Exchange Rate

| Action | Method | Description |
| --- | --- | --- |
| [Get Historical Exchange Rates](actions/get-historical-exchange-rates.md) | GET | Retrieves historical exchange rates from CurrencyAPI. |
| [Get Latest Exchange Rates](actions/get-latest-exchange-rates.md) | GET | Retrieves latest exchange rates from CurrencyAPI. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Get API Status](actions/get-api-status.md) | GET | Retrieves current API quota status from CurrencyAPI. |

