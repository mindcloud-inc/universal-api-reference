# Get Office Weather Stories with National Weather Service

Retrieves office weather stories from National Weather Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/offices/:officeId/weatherstories`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [Get Office Weather Stories](https://api.weather.gov/openapi.json#/paths/~1offices~1{officeId}~1weatherstories/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `officeId` | path | `string` | no | NWS forecast office identifier, such as TOP. |
