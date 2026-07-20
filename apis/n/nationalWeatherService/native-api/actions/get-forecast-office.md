# Get Forecast Office with National Weather Service

Retrieves a forecast office from National Weather Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/offices/:officeId`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [Get Forecast Office](https://api.weather.gov/openapi.json#/paths/~1offices~1{officeId}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `officeId` | path | `string` | no | NWS forecast office identifier, such as TOP. |
