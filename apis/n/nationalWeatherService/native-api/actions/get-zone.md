# Get Zone with National Weather Service

Retrieves a zone from National Weather Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/zones/:type/:zoneId`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [Get Zone](https://api.weather.gov/openapi.json#/paths/~1zones~1{type}~1{zoneId}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `string` | no | NWS zone type, such as forecast, county, or fire. |
| `zoneId` | path | `string` | no | NWS zone identifier, such as KSZ009. |
