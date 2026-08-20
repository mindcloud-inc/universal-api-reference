# Get Service with Centerpoint

## Endpoint

- **Method:** `GET`
- **Path:** `services/:SERVICE_ID`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [Get Service](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/services/{SERVICE_ID}GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `SERVICE_ID` | path | `string` | yes | The service id to retrieve. |
| `fields[productions]` | query | `string` | no | Optional fields productions query parameter. |
| `fields[companies]` | query | `string` | no | Optional fields companies query parameter. |
| `fields[documents]` | query | `string` | no | Optional fields documents query parameter. |
| `fields[employees]` | query | `string` | no | Optional fields employees query parameter. |
| `fields[profiles]` | query | `string` | no | Optional fields profiles query parameter. |
| `fields[buildingDivisions]` | query | `string` | no | Optional fields building divisions query parameter. |
| `fields[properties]` | query | `string` | no | Optional fields properties query parameter. |
| `fields[primaryProposal]` | query | `string` | no | Optional fields primary proposal query parameter. |
| `include` | query | `string` | no | Optional include query parameter. |
