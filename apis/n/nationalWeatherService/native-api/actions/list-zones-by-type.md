# List Zones By Type with National Weather Service

Retrieves zones from National Weather Service by type.

## Endpoint

- **Method:** `GET`
- **Path:** `/zones/:type`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [List Zones By Type](https://api.weather.gov/openapi.json#/paths/~1zones~1{type}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `string` | no | NWS zone type, such as forecast, county, or fire. |
