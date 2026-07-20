# List Station TAFs with National Weather Service

Retrieves station TAFs from National Weather Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/stations/:stationId/tafs`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [List Station TAFs](https://api.weather.gov/openapi.json#/paths/~1stations~1{stationId}~1tafs/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stationId` | path | `string` | no | NWS observation station identifier, such as KDEN. |
