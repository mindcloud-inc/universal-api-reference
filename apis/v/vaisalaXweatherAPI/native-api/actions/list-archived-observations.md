# List Archived Observations with Vaisala Xweather

Retrieves archived observations from Vaisala Xweather API.

## Endpoint

- **Method:** `GET`
- **Path:** `/observations/archive/:id`
- **Base URL:** `https://data.api.xweather.com`
- **Official documentation:** [List Archived Observations](https://www.xweather.com/docs/weather-api/endpoints/observations-archive)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Location, station identifier, postal code, or latitude/longitude. |
| `from` | query | `date` | yes | Archive date to retrieve in YYYY-MM-DD format. |
