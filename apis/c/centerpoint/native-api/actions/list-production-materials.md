# List Production Materials with Centerpoint

## Endpoint

- **Method:** `GET`
- **Path:** `production_materials`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [List Production Materials](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/production_materialsGET)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields[productionMaterials]` | query | `string` | no | Fields: name,cost    On-Demand Feilds: price |
| `fields[productions]` | query | `string` | no | — |
| `fields[companies]` | query | `string` | no | — |
| `fields[materials]` | query | `string` | no | — |
| `include` | query | `string` | no | — |
