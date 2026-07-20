# Get RSI Indicator with Alpha Vantage

Retrieves RSI indicator data from Alpha Vantage.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://www.alphavantage.co`
- **Official documentation:** [Get RSI Indicator](https://www.alphavantage.co/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `series_type` | query | `string` | yes | Query parameter $key for RSI. |
| `time_period` | query | `string` | yes | Query parameter $key for RSI. |
| `symbol` | query | `string` | yes | Query parameter $key for RSI. |
| `interval` | query | `string` | yes | Query parameter $key for RSI. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |
| `time_period` | query | `string` | yes | Number of data points to evaluate. |
| `series_type` | query | `string` | yes | Price series to use. Accepted values: `0`, `1`, `2`, `3`. |
