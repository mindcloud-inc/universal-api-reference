# Get Daily Time Series with Alpha Vantage

Retrieves daily time series data from Alpha Vantage.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://www.alphavantage.co`
- **Official documentation:** [Get Daily Time Series](https://www.alphavantage.co/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputsize` | query | `string` | no | Query parameter $key for TIME_SERIES_DAILY. |
| `symbol` | query | `string` | yes | Query parameter $key for TIME_SERIES_DAILY. |
