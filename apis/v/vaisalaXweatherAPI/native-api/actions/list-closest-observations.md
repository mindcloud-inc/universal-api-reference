# List Closest Observations with Vaisala Xweather

Retrieves closest observations from Vaisala Xweather API.

## Endpoint

- **Method:** `GET`
- **Path:** `/observations/closest`
- **Base URL:** `https://data.api.xweather.com`
- **Official documentation:** [List Closest Observations](https://www.xweather.com/docs/weather-api/endpoints/observations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `p` | query | `string` | yes | Latitude and longitude point for the nearest observations lookup. |
| `limit` | query | `number` | no | Maximum number of nearby observation results to return. |
