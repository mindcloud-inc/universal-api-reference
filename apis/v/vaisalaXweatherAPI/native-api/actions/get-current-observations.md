# Get Current Observations with Vaisala Xweather

Retrieves current observations from Vaisala Xweather API.

## Endpoint

- **Method:** `GET`
- **Path:** `/observations/:id`
- **Base URL:** `https://data.api.xweather.com`
- **Official documentation:** [Get Current Observations](https://www.xweather.com/docs/weather-api/endpoints/observations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Location, place identifier, or latitude/longitude. |
