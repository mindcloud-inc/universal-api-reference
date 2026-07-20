# Get Moving Average with TAAPI.IO

Retrieves Moving Average indicator data from TAAPI.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/ma`
- **Base URL:** `https://api.taapi.io`
- **Official documentation:** [Get Moving Average](https://taapi.io/indicators/moving-average/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `exchange` | query | `string` | yes |
| `symbol` | query | `string` | yes |
| `interval` | query | `string` | yes |
