# Get Observations Along Route with Vaisala Xweather

Retrieves observations along a route from Vaisala Xweather API.

## Endpoint

- **Method:** `GET`
- **Path:** `/observations/route`
- **Base URL:** `https://data.api.xweather.com`
- **Official documentation:** [Get Observations Along Route](https://www.xweather.com/docs/weather-api/endpoints/observations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `p` | query | `string` | yes | Semicolon-delimited route coordinates. |
