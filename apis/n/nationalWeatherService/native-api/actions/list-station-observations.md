# List Station Observations with National Weather Service

Retrieves observations for a National Weather Service station.

## Endpoint

- **Method:** `GET`
- **Path:** `/stations/:stationId/observations`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [List Station Observations](https://api.weather.gov/openapi.json#/paths/~1stations~1{stationId}~1observations/get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stationId` | path | `string` | no | Observation station identifier. |
