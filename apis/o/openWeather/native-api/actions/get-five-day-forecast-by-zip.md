# Get 5 Day Forecast by ZIP with OpenWeather

Retrieves a 5-day forecast from OpenWeather by ZIP code.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/2.5/forecast`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get 5 Day Forecast by ZIP](https://openweathermap.org/forecast5)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zip` | query | `string` | yes | ZIP code with optional country code, for example 94040,us. |
