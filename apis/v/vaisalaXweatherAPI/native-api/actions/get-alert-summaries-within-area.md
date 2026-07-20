# Get Alert Summaries Within Area with Vaisala Xweather

Retrieves alert summaries within an area from Vaisala Xweather API.

## Endpoint

- **Method:** `GET`
- **Path:** `/alerts/summary/within`
- **Base URL:** `https://data.api.xweather.com`
- **Official documentation:** [Get Alert Summaries Within Area](https://www.xweather.com/docs/weather-api/endpoints/alerts-summary)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `p` | query | `string` | yes | Circle center, bounding box, or polygon defining the search area. |
| `radius` | query | `string` | no | Radius used with center-point within searches. |
