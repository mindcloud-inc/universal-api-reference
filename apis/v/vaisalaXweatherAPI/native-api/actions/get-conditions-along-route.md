# Get Conditions Along Route with Vaisala Xweather

Retrieves conditions along a route from Vaisala Xweather API.

## Endpoint

- **Method:** `GET`
- **Path:** `/conditions/route`
- **Base URL:** `https://data.api.xweather.com`
- **Official documentation:** [Get Conditions Along Route](https://www.xweather.com/docs/weather-api/endpoints/conditions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `p` | query | `string` | yes | Semicolon-delimited route points using latitude/longitude pairs. |
