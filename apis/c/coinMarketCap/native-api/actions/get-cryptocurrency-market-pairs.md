# Get Cryptocurrency Market Pairs with CoinMarketCap

Retrieves cryptocurrency market pairs from CoinMarketCap.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/cryptocurrency/market-pairs/latest`
- **Base URL:** `https://pro-api.coinmarketcap.com`
- **Official documentation:** [Get Cryptocurrency Market Pairs](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-crypto)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | CoinMarketCap cryptocurrency ID, for example 1. |
| `limit` | query | `string` | no | Maximum number of market pairs to return. |
