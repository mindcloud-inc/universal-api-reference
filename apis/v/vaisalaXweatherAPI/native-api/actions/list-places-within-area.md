# List Places Within Area with Vaisala Xweather

Retrieves places within an area from Vaisala Xweather API.

## Endpoint

- **Method:** `GET`
- **Path:** `/places/within`
- **Base URL:** `https://data.api.xweather.com`
- **Official documentation:** [List Places Within Area](https://www.xweather.com/docs/weather-api/endpoints/places)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `p` | query | `string` | yes | Circle center, bounding box, or polygon defining the search area. |
| `radius` | query | `string` | no | Radius used with center-point within searches. |
