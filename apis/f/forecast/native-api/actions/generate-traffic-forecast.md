# Generate Traffic Forecast with Forecast

Generates traffic forecasts in Forecast.

## Endpoint

- **Method:** `POST`
- **Path:** `/traffic-forecasting`
- **Base URL:** `https://forecastapi.com/v2`
- **Official documentation:** [Generate Traffic Forecast](https://forecastapi.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `identifier` | body | `string` | yes |
| `data` | body | `list<object>` | yes |
| `periods` | body | `number` | yes |
| `frequency` | body | `string` | yes |
| `traffic_settings.current_capacity` | body | `number` | yes |
| `traffic_settings.baseline_traffic` | body | `number` | yes |
| `data_type` | body | `string` | no |
| `confidence_level` | body | `number` | no |
| `data[].date` | body | `string` | yes |
| `data[].value` | body | `number` | yes |
