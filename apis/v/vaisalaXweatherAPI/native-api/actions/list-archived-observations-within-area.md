# List Archived Observations Within Area with Vaisala Xweather

Retrieves archived observations within an area from Vaisala Xweather API.

## Endpoint

- **Method:** `GET`
- **Path:** `/observations/archive/within`
- **Base URL:** `https://data.api.xweather.com`
- **Official documentation:** [List Archived Observations Within Area](https://www.xweather.com/docs/weather-api/endpoints/observations-archive)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `p` | query | `string` | yes | Circle center, bounding box, or polygon defining the search area. |
| `from` | query | `date` | yes | Archive date to retrieve in YYYY-MM-DD format. |
| `radius` | query | `string` | no | Radius used with center-point within searches. |
