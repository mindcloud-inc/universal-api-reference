# Get Current Conditions with Vaisala Xweather

Retrieves current conditions from Vaisala Xweather API.

## Endpoint

- **Method:** `GET`
- **Path:** `/conditions/:id`
- **Base URL:** `https://data.api.xweather.com`
- **Official documentation:** [Get Current Conditions](https://www.xweather.com/docs/weather-api/endpoints/conditions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Location, place identifier, or latitude/longitude. |
