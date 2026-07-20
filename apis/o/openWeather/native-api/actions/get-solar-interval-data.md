# Get Solar Interval Data with OpenWeather

Retrieves solar interval data from OpenWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.openweathermap.org/energy/2.0/location/:locationId/interval_data`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Solar Interval Data](https://openweathermap.org/api/solar-panels-and-energy-prediction-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationId` | path | `string` | yes | Solar location identifier. |
| `date` | query | `string` | yes | Date to retrieve interval data for. |
| `interval` | query | `string` | yes | Requested interval granularity. |
