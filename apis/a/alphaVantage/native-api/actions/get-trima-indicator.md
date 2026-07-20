# Get TRIMA Indicator with Alpha Vantage

Retrieves TRIMA indicator data from Alpha Vantage.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://www.alphavantage.co`
- **Official documentation:** [Get TRIMA Indicator](https://www.alphavantage.co/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `interval` | query | `string` | yes | Query parameter $key for TRIMA. |
| `series_type` | query | `string` | yes | Query parameter $key for TRIMA. |
| `symbol` | query | `string` | yes | Query parameter $key for TRIMA. |
| `time_period` | query | `string` | yes | Query parameter $key for TRIMA. |
