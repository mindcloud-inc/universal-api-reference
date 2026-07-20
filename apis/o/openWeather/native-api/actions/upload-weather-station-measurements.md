# Upload Weather Station Measurements with OpenWeather

Uploads weather station measurements to OpenWeather.

## Endpoint

- **Method:** `POST`
- **Path:** `/data/3.0/measurements`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Upload Weather Station Measurements](https://openweathermap.org/stations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `measurements[]` | body | `array<object>` | yes | Array of measurement objects to upload for a station. |
