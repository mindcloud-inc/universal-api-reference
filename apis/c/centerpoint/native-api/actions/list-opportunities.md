# List Opportunities with Centerpoint

## Endpoint

- **Method:** `GET`
- **Path:** `opportunities`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [List Opportunities](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/opportunitiesGET)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[updatedAt]` | query | `string` | no | — |
| `filter[updatedAt][gte]` | query | `string` | no | — |
| `include` | query | `string` | no | — |
| `fields[productions]` | query | `string` | no | Optional fields productions query parameter. |
| `fields[properties]` | query | `string` | no | Optional fields properties query parameter. |
| `fields[companies]` | query | `string` | no | Optional fields companies query parameter. |
| `fields[profiles]` | query | `string` | no | Optional fields profiles query parameter. |
| `fields[employees]` | query | `string` | no | Optional fields employees query parameter. |
| `fields[leadTypes]` | query | `string` | no | Optional fields lead types query parameter. |
| `fields[workflowStages]` | query | `string` | no | Optional fields workflow stages query parameter. |
| `fields[buildingDivisions]` | query | `string` | no | Optional fields building divisions query parameter. |
| `reports[0]` | query | `string` | no | Optional reports 0 query parameter. |
| `reports[1]` | query | `string` | no | Optional reports 1 query parameter. |
| `reports[2]` | query | `string` | no | Optional reports 2 query parameter. |
