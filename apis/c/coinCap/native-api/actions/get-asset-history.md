# Get Asset History with CoinCap

Retrieves historical data for an asset from CoinCap.

## Endpoint

- **Method:** `GET`
- **Path:** `/assets/:slug/history`
- **Base URL:** `https://rest.coincap.io/v3`
- **Official documentation:** [Get Asset History](https://pro.coincap.io/api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | The asset slug to retrieve history for. |
| `interval` | query | `string` | yes | The interval to return. Supported values are m1, m5, m15, m30, h1, h2, h6, h12, and d1. |
| `start` | query | `number` | no | Start timestamp in milliseconds. |
| `end` | query | `number` | no | End timestamp in milliseconds. |
