# Get Exchange Market Pairs with CoinMarketCap

Retrieves exchange market pairs from CoinMarketCap.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/exchange/market-pairs/latest`
- **Base URL:** `https://pro-api.coinmarketcap.com`
- **Official documentation:** [Get Exchange Market Pairs](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-exchange)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | CoinMarketCap exchange ID, for example 270. |
| `limit` | query | `string` | no | Maximum number of exchange market pairs to return. |
