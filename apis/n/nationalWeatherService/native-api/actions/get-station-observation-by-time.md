# Get Station Observation By Time with National Weather Service

Retrieves a station observation from National Weather Service by time.

## Endpoint

- **Method:** `GET`
- **Path:** `/stations/:stationId/observations/:time`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [Get Station Observation By Time](https://api.weather.gov/openapi.json#/paths/~1stations~1{stationId}~1observations~1{time}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stationId` | path | `string` | no | Observation station identifier. |
| `time` | path | `string` | no | Observation timestamp from the station observation feed. |
