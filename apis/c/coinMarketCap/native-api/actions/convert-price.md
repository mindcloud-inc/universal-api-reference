# Convert Price with CoinMarketCap

Converts amounts between currencies using CoinMarketCap pricing.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/tools/price-conversion`
- **Base URL:** `https://pro-api.coinmarketcap.com`
- **Official documentation:** [Convert Price](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-market)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | query | `string` | no | Amount to convert. |
| `convert` | query | `string` | no | Target conversion currency symbol, for example USD. |
| `symbol` | query | `string` | no | Source cryptocurrency symbol, for example BTC. |
