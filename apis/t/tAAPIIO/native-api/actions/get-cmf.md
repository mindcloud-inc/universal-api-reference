# Get Chaikin Money Flow with TAAPI.IO

Retrieves Chaikin Money Flow indicator data from TAAPI.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/cmf`
- **Base URL:** `https://api.taapi.io`
- **Official documentation:** [Get Chaikin Money Flow](https://taapi.io/indicators/chaikin-money-flow/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `exchange` | query | `string` | yes |
| `symbol` | query | `string` | yes |
| `interval` | query | `string` | yes |
