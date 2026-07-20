# List Products By Type with National Weather Service

Retrieves text products from National Weather Service by type.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/types/:typeId`
- **Base URL:** `https://api.weather.gov`
- **Official documentation:** [List Products By Type](https://api.weather.gov/openapi.json#/paths/~1products~1types~1{typeId}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `typeId` | path | `string` | no | NWS text product type identifier, such as AFD. |
