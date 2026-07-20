# List Observations Within Area with Vaisala Xweather

Retrieves observations within an area from Vaisala Xweather API.

## Endpoint

- **Method:** `GET`
- **Path:** `/observations/within`
- **Base URL:** `https://data.api.xweather.com`
- **Official documentation:** [List Observations Within Area](https://www.xweather.com/docs/weather-api/endpoints/observations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `p` | query | `string` | yes | Point, radius, or area geometry for the observations lookup. |
| `radius` | query | `string` | no | Radius around the point or area center. |
