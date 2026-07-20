# List Zone Forecast Observations with National Weather Service

Retrieves observations for a National Weather Service forecast zone.

## Endpoint

- **Method:** `GET`
- **Path:** `/zones/forecast/:zoneId/observations`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [List Zone Forecast Observations](https://api.weather.gov/openapi.json#/paths/~1zones~1forecast~1{zoneId}~1observations/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zoneId` | path | `string` | no | NWS forecast zone identifier, such as KSZ009. |
