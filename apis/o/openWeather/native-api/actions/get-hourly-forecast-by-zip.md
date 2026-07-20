# Get Hourly Forecast by ZIP with OpenWeather

Retrieves an hourly forecast from OpenWeather by ZIP code.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/2.5/forecast/hourly`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Hourly Forecast by ZIP](https://openweathermap.org/api/hourly-forecast)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zip` | query | `string` | yes | ZIP code with optional country code, for example 94040,us. |
