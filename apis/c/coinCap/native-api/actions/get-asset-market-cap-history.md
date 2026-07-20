# Get Asset Market Cap History with CoinCap

Retrieves market cap history for an asset from CoinCap.

## Endpoint

- **Method:** `GET`
- **Path:** `/assets/:slug/marketcap-history`
- **Base URL:** `https://rest.coincap.io/v3`
- **Official documentation:** [Get Asset Market Cap History](https://pro.coincap.io/api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | The asset slug to retrieve market cap history for. |
| `start` | query | `number` | no | Start timestamp in milliseconds. |
| `end` | query | `number` | no | End timestamp in milliseconds. |
