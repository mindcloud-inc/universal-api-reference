# Get Material with Centerpoint

## Endpoint

- **Method:** `GET`
- **Path:** `materials/:MATERIAL_ID`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [Get Material](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/materials/{MATERIAL_ID}GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MATERIAL_ID` | path | `number` | yes | The material id to retrieve. |
| `include` | query | `string` | no | Optional include query parameter. |
