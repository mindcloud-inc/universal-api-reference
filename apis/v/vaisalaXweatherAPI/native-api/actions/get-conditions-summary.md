# Get Conditions Summary with Vaisala Xweather

Retrieves conditions summary data from Vaisala Xweather API.

## Endpoint

- **Method:** `GET`
- **Path:** `/conditions/summary/:id`
- **Base URL:** `https://data.api.xweather.com`
- **Official documentation:** [Get Conditions Summary](https://www.xweather.com/docs/weather-api/endpoints/conditions-summary)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Location, station identifier, postal code, or latitude/longitude. |
| `from` | query | `date` | yes | Start date for the summary window in YYYY-MM-DD format. |
| `to` | query | `date` | no | End date for the summary window in YYYY-MM-DD format. |
