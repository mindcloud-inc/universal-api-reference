# List Active Alerts By Area with National Weather Service

Retrieves active alerts from National Weather Service by area.

## Endpoint

- **Method:** `GET`
- **Path:** `/alerts/active/area/:area`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [List Active Alerts By Area](https://api.weather.gov/openapi.json#/paths/~1alerts~1active~1area~1{area}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `area` | path | `string` | no | State or marine area code. |
