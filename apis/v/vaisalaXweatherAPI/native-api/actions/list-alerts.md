# List Alerts with Vaisala Xweather

Retrieves alerts from Vaisala Xweather API.

## Endpoint

- **Method:** `GET`
- **Path:** `/alerts/:id`
- **Base URL:** `https://data.api.xweather.com`
- **Official documentation:** [List Alerts](https://www.xweather.com/docs/weather-api/endpoints/alerts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Location, place identifier, or latitude/longitude. |
