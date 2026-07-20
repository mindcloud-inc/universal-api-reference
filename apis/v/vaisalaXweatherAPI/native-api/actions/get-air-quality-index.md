# Get Air Quality Index with Vaisala Xweather

Retrieves air quality index data from Vaisala Xweather API.

## Endpoint

- **Method:** `GET`
- **Path:** `/airquality/index/:id`
- **Base URL:** `https://data.api.xweather.com`
- **Official documentation:** [Get Air Quality Index](https://www.xweather.com/docs/weather-api/endpoints/airquality-index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Location, place identifier, or latitude/longitude. |
