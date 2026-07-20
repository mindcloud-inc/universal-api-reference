# Delete Solar Panel with OpenWeather

Deletes a solar panel from OpenWeather.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://api.openweathermap.org/energy/2.0/panel/:panelId`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Delete Solar Panel](https://openweathermap.org/api/solar-panels-and-energy-prediction-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `panelId` | path | `string` | yes | Solar panel identifier. |
