# Get Latest Station Observation with National Weather Service

Retrieves the latest observation for a National Weather Service station.

## Endpoint

- **Method:** `GET`
- **Path:** `/stations/:stationId/observations/latest`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [Get Latest Station Observation](https://api.weather.gov/openapi.json#/paths/~1stations~1{stationId}~1observations~1latest/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stationId` | path | `string` | no | Observation station identifier. |
