# Get Observation Station with National Weather Service

Retrieves an observation station from National Weather Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/stations/:stationId`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [Get Observation Station](https://api.weather.gov/openapi.json#/paths/~1stations~1{stationId}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stationId` | path | `string` | no | Observation station identifier. |
