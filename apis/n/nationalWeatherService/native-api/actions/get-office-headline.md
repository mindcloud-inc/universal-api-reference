# Get Office Headline with National Weather Service

Retrieves an office headline from National Weather Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/offices/:officeId/headlines/:headlineId`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [Get Office Headline](https://api.weather.gov/openapi.json#/paths/~1offices~1{officeId}~1headlines~1{headlineId}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `headlineId` | path | `string` | no | NWS office headline identifier. |
| `officeId` | path | `string` | no | NWS forecast office identifier, such as BOU. |
