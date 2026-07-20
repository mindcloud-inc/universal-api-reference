# Get Solar Location with OpenWeather

Retrieves a solar location from OpenWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.openweathermap.org/energy/2.0/location/:locationId`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Solar Location](https://openweathermap.org/api/solar-panels-and-energy-prediction-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationId` | path | `string` | yes | Solar location identifier. |
