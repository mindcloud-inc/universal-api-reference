# List Office Headlines with National Weather Service

Retrieves office headlines from National Weather Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/offices/:officeId/headlines`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [List Office Headlines](https://api.weather.gov/openapi.json#/paths/~1offices~1{officeId}~1headlines/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `officeId` | path | `string` | no | NWS forecast office identifier, such as BOU. |
