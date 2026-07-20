# Get Current Weather by ZIP with OpenWeather

Retrieves current weather from OpenWeather by ZIP code.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/2.5/weather`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Current Weather by ZIP](https://openweathermap.org/current)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zip` | query | `string` | yes | ZIP code with optional country code, for example 94040,us. |
