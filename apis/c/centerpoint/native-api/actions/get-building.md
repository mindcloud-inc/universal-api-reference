# Get Building with Centerpoint

## Endpoint

- **Method:** `GET`
- **Path:** `buildings/:BUILDING_ID`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [Get Building](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/buildings/BUILDING_IDGET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `BUILDING_ID` | path | `number` | yes | — |
| `fields[properties]` | query | `string` | no | — |
| `fields[buildings]` | query | `string` | no | — |
| `include` | query | `string` | no | e.g. property,divisions,divisions.outlines,divisions.productTemplateTag |
