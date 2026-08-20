# Get Company with Centerpoint

## Endpoint

- **Method:** `GET`
- **Path:** `companies/:COMPANY_ID`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [Get Company](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/companies/{COMPANY_ID}GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `COMPANY_ID` | path | `string` | yes | — |
| `fields[companies]` | query | `string` | no | Optional fields companies query parameter. |
| `fields[profiles]` | query | `string` | no | Optional fields profiles query parameter. |
| `fields[employees]` | query | `string` | no | Optional fields employees query parameter. |
| `include` | query | `string` | no | Optional include query parameter. |
