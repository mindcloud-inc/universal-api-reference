# Get Alert with National Weather Service

Retrieves an alert from National Weather Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/alerts/:id`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [Get Alert](https://api.weather.gov/openapi.json#/paths/~1alerts~1{id}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | NWS alert identifier. |
