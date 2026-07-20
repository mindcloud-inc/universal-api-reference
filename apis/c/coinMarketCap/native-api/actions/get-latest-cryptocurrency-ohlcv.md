# Get Latest Cryptocurrency OHLCV with CoinMarketCap

Retrieves latest cryptocurrency OHLCV data from CoinMarketCap.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/cryptocurrency/ohlcv/latest`
- **Base URL:** `https://pro-api.coinmarketcap.com`
- **Official documentation:** [Get Latest Cryptocurrency OHLCV](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-crypto)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | CoinMarketCap cryptocurrency ID, for example 1. |
