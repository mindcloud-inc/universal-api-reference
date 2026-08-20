# List Productions with Centerpoint

## Endpoint

- **Method:** `GET`
- **Path:** `productions`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [List Productions](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/productionsGET)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[updated_at][gt]` | query | `string` | no | Example: 2025-01-13 10:00:00 |
| `filter[updated_at][lt]` | query | `string` | no | — |
| `include` | query | `string` | no | — |
| `fields[productions]` | query | `string` | no | Optional fields productions query parameter. |
| `fields[properties]` | query | `string` | no | Optional fields properties query parameter. |
| `fields[buildingDivisions]` | query | `string` | no | Optional fields building divisions query parameter. |
| `fields[companies]` | query | `string` | no | Optional fields companies query parameter. |
| `fields[profiles]` | query | `string` | no | Optional fields profiles query parameter. |
| `fields[employees]` | query | `string` | no | Optional fields employees query parameter. |
| `fields[locations]` | query | `string` | no | Optional fields locations query parameter. |
| `fields[subcontractorProfiles]` | query | `string` | no | Optional fields subcontractor profiles query parameter. |
| `fields[workflowStages]` | query | `string` | no | Optional fields workflow stages query parameter. |
