# Get Solar Panel with OpenWeather

Retrieves a solar panel from OpenWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.openweathermap.org/energy/2.0/panel/:panelId`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Solar Panel](https://openweathermap.org/api/solar-panels-and-energy-prediction-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `panelId` | path | `string` | yes | Solar panel identifier. |
