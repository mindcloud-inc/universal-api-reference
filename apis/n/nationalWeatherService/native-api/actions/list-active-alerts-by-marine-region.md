# List Active Alerts By Marine Region with National Weather Service

Retrieves active alerts from National Weather Service by marine region.

## Endpoint

- **Method:** `GET`
- **Path:** `/alerts/active/region/:region`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [List Active Alerts By Marine Region](https://api.weather.gov/openapi.json#/paths/~1alerts~1active~1region~1{region}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `region` | path | `string` | no | NWS marine region code. |
