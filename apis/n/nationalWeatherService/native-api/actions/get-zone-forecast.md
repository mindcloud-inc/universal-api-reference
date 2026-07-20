# Get Zone Forecast with National Weather Service

Retrieves a zone forecast from National Weather Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/zones/:type/:zoneId/forecast`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [Get Zone Forecast](https://api.weather.gov/openapi.json#/paths/~1zones~1{type}~1{zoneId}~1forecast/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `string` | no | NWS zone type, such as forecast. |
| `zoneId` | path | `string` | no | NWS zone identifier, such as KSZ009. |
