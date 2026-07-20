# Get Bollinger Bands with TAAPI.IO

Retrieves Bollinger Bands indicator data from TAAPI.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/bbands`
- **Base URL:** `https://api.taapi.io`
- **Official documentation:** [Get Bollinger Bands](https://taapi.io/indicators/bollinger-bands/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `exchange` | query | `string` | yes |
| `symbol` | query | `string` | yes |
| `interval` | query | `string` | yes |
