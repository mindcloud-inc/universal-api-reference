# Get Historical CMC100 Index with CoinMarketCap

Retrieves historical CMC100 index values from CoinMarketCap.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/index/cmc100-historical`
- **Base URL:** `https://pro-api.coinmarketcap.com`
- **Official documentation:** [Get Historical CMC100 Index](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-market)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `string` | no | Number of historical CMC100 points to return. |
| `interval` | query | `string` | no | Historical interval such as daily. |
