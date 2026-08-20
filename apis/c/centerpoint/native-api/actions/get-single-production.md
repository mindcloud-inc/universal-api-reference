# Get Production with Centerpoint

## Endpoint

- **Method:** `GET`
- **Path:** `productions/:PRODUCTION_ID`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [Get Production](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/productions/{PRODUCTION_ID}GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PRODUCTION_ID` | path | `string` | yes | — |
| `fields[companies]` | query | `string` | no | Optional fields companies query parameter. |
| `fields[employees]` | query | `string` | no | Optional fields employees query parameter. |
| `fields[profiles]` | query | `string` | no | Optional fields profiles query parameter. |
| `fields[productionDays]` | query | `string` | no | Optional fields production days query parameter. |
| `fields[properties]` | query | `string` | no | Optional fields properties query parameter. |
| `include` | query | `string` | no | Optional include query parameter. |
