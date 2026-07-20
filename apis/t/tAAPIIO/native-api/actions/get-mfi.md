# Get Money Flow Index with TAAPI.IO

Retrieves Money Flow Index indicator data from TAAPI.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/mfi`
- **Base URL:** `https://api.taapi.io`
- **Official documentation:** [Get Money Flow Index](https://taapi.io/indicators/money-flow-index/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `exchange` | query | `string` | yes |
| `symbol` | query | `string` | yes |
| `interval` | query | `string` | yes |
