# Generate Forecast with Forecast

Generates forecasts in Forecast.

## Endpoint

- **Method:** `POST`
- **Path:** `/forecast`
- **Base URL:** `https://forecastapi.com/v2`
- **Official documentation:** [Generate Forecast](https://forecastapi.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | body | `string` | yes | Unique identifier for the data series, such as a SKU or product ID. |
| `data` | body | `list<object>` | yes | Time series datapoints to forecast from. |
| `periods` | body | `number` | yes | Number of forecast periods to generate. |
| `frequency` | body | `string` | yes | Data frequency: D, W, M, Q, Y, or H. |
| `data_type` | body | `string` | no | Optional data type for optimized model selection. |
| `confidence_level` | body | `number` | no | Optional confidence level for forecast intervals. |
| `data[].date` | body | `string` | yes | Date for one datapoint in YYYY-MM-DD format, for example 2024-01-01. |
| `data[].value` | body | `number` | yes | Numeric value for one datapoint. |
