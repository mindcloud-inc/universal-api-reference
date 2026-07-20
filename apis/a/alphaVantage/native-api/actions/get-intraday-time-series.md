# Get Intraday Time Series with Alpha Vantage

Retrieves intraday time series data from Alpha Vantage.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://www.alphavantage.co`
- **Official documentation:** [Get Intraday Time Series](https://www.alphavantage.co/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `interval` | query | `string` | yes | Query parameter $key for TIME_SERIES_INTRADAY. |
| `month` | query | `string` | no | Query parameter $key for TIME_SERIES_INTRADAY. |
| `outputsize` | query | `string` | no | Query parameter $key for TIME_SERIES_INTRADAY. |
| `symbol` | query | `string` | yes | Query parameter $key for TIME_SERIES_INTRADAY. |
