# Get Climatic Forecast by ZIP with OpenWeather

Retrieves a 30-day climate forecast from OpenWeather by ZIP code.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/2.5/forecast/climate`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Climatic Forecast by ZIP](https://openweathermap.org/api/forecast30)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zip` | query | `string` | yes | ZIP or postal code with optional country code suffix. |
