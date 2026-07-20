# Get Alert Summary with Vaisala Xweather

Retrieves alert summary data from Vaisala Xweather API.

## Endpoint

- **Method:** `GET`
- **Path:** `/alerts/summary/:id`
- **Base URL:** `https://data.api.xweather.com`
- **Official documentation:** [Get Alert Summary](https://www.xweather.com/docs/weather-api/endpoints/alerts-summary)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Location, postal code, or latitude/longitude for alert summary lookup. |
