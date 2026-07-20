# Get VWAP Indicator with Alpha Vantage

Retrieves VWAP indicator data from Alpha Vantage.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://www.alphavantage.co`
- **Official documentation:** [Get VWAP Indicator](https://www.alphavantage.co/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `interval` | query | `string` | yes | Query parameter $key for VWAP. |
| `symbol` | query | `string` | yes | Query parameter $key for VWAP. |
