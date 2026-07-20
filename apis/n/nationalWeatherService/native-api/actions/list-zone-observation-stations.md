# List Zone Observation Stations with National Weather Service

Retrieves observation stations for a National Weather Service zone.

## Endpoint

- **Method:** `GET`
- **Path:** `/zones/forecast/:zoneId/stations`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [List Zone Observation Stations](https://api.weather.gov/openapi.json#/paths/~1zones~1forecast~1{zoneId}~1stations/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zoneId` | path | `string` | no | NWS forecast zone identifier, such as KSZ009. |
