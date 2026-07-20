# Get Daily Forecast by ZIP with OpenWeather

Retrieves a daily forecast from OpenWeather by ZIP code.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/2.5/forecast/daily`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Daily Forecast by ZIP](https://openweathermap.org/forecast16)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zip` | query | `string` | yes | ZIP or postal code with optional country code suffix. |
