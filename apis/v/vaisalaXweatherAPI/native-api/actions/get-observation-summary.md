# Get Observation Summary with Vaisala Xweather

Retrieves observation summary data from Vaisala Xweather API.

## Endpoint

- **Method:** `GET`
- **Path:** `/observations/summary/:id`
- **Base URL:** `https://data.api.xweather.com`
- **Official documentation:** [Get Observation Summary](https://www.xweather.com/docs/weather-api/endpoints/observations-summary)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Location, station identifier, postal code, or latitude/longitude. |
| `from` | query | `date` | yes | Start date for the summary window in YYYY-MM-DD format. |
| `to` | query | `date` | no | End date for the summary window in YYYY-MM-DD format. |
