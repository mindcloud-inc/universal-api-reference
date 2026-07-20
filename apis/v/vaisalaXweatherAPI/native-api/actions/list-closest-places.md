# List Closest Places with Vaisala Xweather

Retrieves closest places from Vaisala Xweather API.

## Endpoint

- **Method:** `GET`
- **Path:** `/places/closest`
- **Base URL:** `https://data.api.xweather.com`
- **Official documentation:** [List Closest Places](https://www.xweather.com/docs/weather-api/endpoints/places)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `p` | query | `string` | yes | Latitude/longitude or place to search from. |
| `limit` | query | `number` | no | Maximum number of nearby places to return. |
