# Get Office Briefing with National Weather Service

Retrieves an office briefing from National Weather Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/offices/:officeId/briefing`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [Get Office Briefing](https://api.weather.gov/openapi.json#/paths/~1offices~1{officeId}~1briefing/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `officeId` | path | `string` | no | NWS forecast office identifier, such as TOP. |
