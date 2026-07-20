# <img src="https://images.mindcloud.co/apps/icons/oanda_1775578750138.png" alt="Oanda logo" width="28" height="28"> Oanda: Universal API

Get OANDA Exchange Rates API datasets, currencies, historical rates, supported forwards, remaining quote usage, streams, and book snapshots.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/oanda/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.oanda.com/foreign-exchange-data-services/en/exchange-rates-api/
- **Vendor API docs:** https://exchange-rates-api.oanda.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Remaining Quotes](actions/get-remaining-quotes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oanda/latest/actions/get-remaining-quotes?connectionId=$CONNECTION_ID&ext=json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Currency

| Action | Method | Description |
| --- | --- | --- |
| [List Currencies](actions/list-currencies.md) | GET | Retrieves supported currency codes from Oanda. |

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [Get Dataset](actions/get-dataset.md) | GET | Retrieves exchange-rate dataset details from Oanda. |

### Exchange Rates

| Action | Method | Description |
| --- | --- | --- |
| [Get Aggregated Rates](actions/get-aggregated-rates.md) | GET | Retrieves aggregated candle rates from Oanda. |
| [Get Candle Rate](actions/get-candle-rate.md) | GET | Retrieves one daily candle rate from Oanda. |
| [Get Candle Series](actions/get-candle-series.md) | GET | Retrieves daily candle rates from Oanda over a time range. |
| [Get Forward Rate](actions/get-forward-rate.md) | GET | Retrieves forward rates from Oanda by tenor. |
| [Get Rates](actions/get-rates.md) | GET | Retrieves exchange rates from Oanda for one base currency. |
| [Get Spot Rates](actions/get-spot-rates.md) | GET | Retrieves spot exchange rates from Oanda. |
| [Get Supported Forwards](actions/get-supported-forwards.md) | GET | Retrieves supported forward tenors from Oanda. |
| [Stream Rates](actions/stream-rates.md) | GET | Streams live exchange rates from Oanda. |

### Order Book

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Book](actions/get-order-book.md) | GET | Retrieves order book snapshots from Oanda. |

### Position Book

| Action | Method | Description |
| --- | --- | --- |
| [Get Position Book](actions/get-position-book.md) | GET | Retrieves position book snapshots from Oanda. |

### Usage Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get Remaining Quotes](actions/get-remaining-quotes.md) | GET | Retrieves remaining quote usage from Oanda. |

