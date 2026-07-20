# Get Cryptocurrency Price Performance Stats with CoinMarketCap

Retrieves cryptocurrency price performance stats from CoinMarketCap.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/cryptocurrency/price-performance-stats/latest`
- **Base URL:** `https://pro-api.coinmarketcap.com`
- **Official documentation:** [Get Cryptocurrency Price Performance Stats](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-crypto)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | CoinMarketCap cryptocurrency ID, for example 1. |
