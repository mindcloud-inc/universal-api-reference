# Get Rate of Change with TAAPI.IO

Retrieves Rate of Change indicator data from TAAPI.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/roc`
- **Base URL:** `https://api.taapi.io`
- **Official documentation:** [Get Rate of Change](https://taapi.io/indicators/rate-of-change/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `exchange` | query | `string` | yes |
| `symbol` | query | `string` | yes |
| `interval` | query | `string` | yes |
