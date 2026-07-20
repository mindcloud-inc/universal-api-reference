# Get Most Visited Cryptocurrencies with CoinMarketCap

Retrieves most visited cryptocurrencies from CoinMarketCap.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/cryptocurrency/trending/most-visited`
- **Base URL:** `https://pro-api.coinmarketcap.com`
- **Official documentation:** [Get Most Visited Cryptocurrencies](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-crypto)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `string` | no | Maximum number of most-visited cryptocurrencies to return. |
