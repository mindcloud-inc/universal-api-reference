# Get Latest Product By Type And Location with National Weather Service

Retrieves the latest text product from National Weather Service by type and location.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/types/:typeId/locations/:locationId/latest`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [Get Latest Product By Type And Location](https://api.weather.gov/openapi.json#/paths/~1products~1types~1{typeId}~1locations~1{locationId}~1latest/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationId` | path | `string` | no | NWS text product location identifier, such as TOP. |
| `typeId` | path | `string` | no | NWS text product type identifier, such as AFD. |
