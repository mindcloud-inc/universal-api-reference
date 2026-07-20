# Get DX Indicator with Alpha Vantage

Retrieves DX indicator data from Alpha Vantage.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://www.alphavantage.co`
- **Official documentation:** [Get DX Indicator](https://www.alphavantage.co/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `interval` | query | `string` | yes | Query parameter $key for DX. |
| `symbol` | query | `string` | yes | Query parameter $key for DX. |
| `time_period` | query | `string` | yes | Query parameter $key for DX. |
