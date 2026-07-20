# List Closest Archived Observations with Vaisala Xweather

Retrieves closest archived observations from Vaisala Xweather API.

## Endpoint

- **Method:** `GET`
- **Path:** `/observations/archive/closest`
- **Base URL:** `https://data.api.xweather.com`
- **Official documentation:** [List Closest Archived Observations](https://www.xweather.com/docs/weather-api/endpoints/observations-archive)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `p` | query | `string` | yes | Latitude/longitude or place to search from. |
| `from` | query | `date` | yes | Archive date to retrieve in YYYY-MM-DD format. |
| `limit` | query | `number` | no | Maximum number of archived observations to return. |
