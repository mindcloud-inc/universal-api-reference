# Get SMA Indicator with Alpha Vantage

Retrieves SMA indicator data from Alpha Vantage.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://www.alphavantage.co`
- **Official documentation:** [Get SMA Indicator](https://www.alphavantage.co/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `series_type` | query | `string` | yes | Query parameter $key for SMA. |
| `time_period` | query | `string` | yes | Query parameter $key for SMA. |
| `symbol` | query | `string` | yes | Query parameter $key for SMA. |
| `interval` | query | `string` | yes | Query parameter $key for SMA. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |
| `time_period` | query | `string` | yes | Number of data points to average. |
| `series_type` | query | `string` | yes | Price series to use. Accepted values: `0`, `1`, `2`, `3`. |
