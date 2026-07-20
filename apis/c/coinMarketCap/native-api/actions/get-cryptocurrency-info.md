# Get Cryptocurrency Info with CoinMarketCap

Retrieves cryptocurrency metadata from CoinMarketCap.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/cryptocurrency/info`
- **Base URL:** `https://pro-api.coinmarketcap.com`
- **Official documentation:** [Get Cryptocurrency Info](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-crypto)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | CoinMarketCap cryptocurrency ID, for example 1. |
