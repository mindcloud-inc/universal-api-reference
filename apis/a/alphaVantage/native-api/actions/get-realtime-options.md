# Get Realtime Options with Alpha Vantage

Retrieves realtime options data from Alpha Vantage.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://www.alphavantage.co`
- **Official documentation:** [Get Realtime Options](https://www.alphavantage.co/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contract` | query | `string` | no | Query parameter $key for REALTIME_OPTIONS. |
| `require_greeks` | query | `string` | no | Query parameter $key for REALTIME_OPTIONS. |
| `symbol` | query | `string` | yes | Query parameter $key for REALTIME_OPTIONS. |
