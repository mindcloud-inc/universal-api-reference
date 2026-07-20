# List Active Alerts By Zone with National Weather Service

Retrieves active alerts from National Weather Service by zone.

## Endpoint

- **Method:** `GET`
- **Path:** `/alerts/active/zone/:zoneId`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [List Active Alerts By Zone](https://api.weather.gov/openapi.json#/paths/~1alerts~1active~1zone~1{zoneId}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zoneId` | path | `string` | no | NWS public, county, fire, or marine zone ID. |
