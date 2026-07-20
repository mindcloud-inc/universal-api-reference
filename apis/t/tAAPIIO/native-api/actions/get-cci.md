# Get Commodity Channel Index with TAAPI.IO

Retrieves Commodity Channel Index indicator data from TAAPI.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/cci`
- **Base URL:** `https://api.taapi.io`
- **Official documentation:** [Get Commodity Channel Index](https://taapi.io/indicators/commodity-channel-index/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `exchange` | query | `string` | yes |
| `symbol` | query | `string` | yes |
| `interval` | query | `string` | yes |
