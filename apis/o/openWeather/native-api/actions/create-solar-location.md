# Create Solar Location with OpenWeather

Creates a solar location in OpenWeather.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.openweathermap.org/energy/2.0/locations`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Create Solar Location](https://openweathermap.org/api/solar-panels-and-energy-prediction-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `coordinates` | body | `object` | yes | GeoJSON point coordinates for the solar location. |
