# List Solar Panels with OpenWeather

Lists solar panels in OpenWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.openweathermap.org/energy/2.0/location/:locationId/panels`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [List Solar Panels](https://openweathermap.org/api/solar-panels-and-energy-prediction-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationId` | path | `string` | yes | Solar location identifier. |
