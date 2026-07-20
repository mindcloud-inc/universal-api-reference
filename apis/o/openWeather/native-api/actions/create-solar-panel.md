# Create Solar Panel with OpenWeather

Creates a solar panel in OpenWeather.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.openweathermap.org/energy/2.0/location/:locationId/panels`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Create Solar Panel](https://openweathermap.org/api/solar-panels-and-energy-prediction-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationId` | path | `string` | yes | Solar location identifier. |
| `type` | body | `string` | yes | Solar panel type. |
| `area` | body | `number` | yes | Panel area in square meters. |
| `tilt` | body | `number` | yes | Panel tilt in degrees. |
| `azimuth` | body | `number` | yes | Panel azimuth in degrees. |
| `peak_power` | body | `number` | yes | Peak power in kilowatts. |
