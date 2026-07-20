# Get Historical Cryptocurrency Quotes with CoinMarketCap

Retrieves historical cryptocurrency quotes from CoinMarketCap.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/cryptocurrency/quotes/historical`
- **Base URL:** `https://pro-api.coinmarketcap.com`
- **Official documentation:** [Get Historical Cryptocurrency Quotes](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-crypto)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | CoinMarketCap cryptocurrency ID, for example 1. |
| `interval` | query | `string` | no | Historical interval such as daily. |
| `time_end` | query | `string` | no | End date or timestamp for the historical window. |
| `time_start` | query | `string` | no | Start date or timestamp for the historical window. |
