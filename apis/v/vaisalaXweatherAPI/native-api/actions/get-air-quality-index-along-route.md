# Get Air Quality Index Along Route with Vaisala Xweather

Retrieves air quality index data along a route from Vaisala Xweather API.

## Endpoint

- **Method:** `GET`
- **Path:** `/airquality/index/route`
- **Base URL:** `https://data.api.xweather.com`
- **Official documentation:** [Get Air Quality Index Along Route](https://www.xweather.com/docs/weather-api/endpoints/airquality-index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `p` | query | `string` | yes | Semicolon-delimited route coordinates. |
