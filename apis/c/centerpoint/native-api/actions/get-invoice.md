# Get Invoice with Centerpoint

## Endpoint

- **Method:** `GET`
- **Path:** `invoices/:INVOICE_ID`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [Get Invoice](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/invoices/{INVOICE_ID}GET)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `INVOICE_ID` | path | `string` | yes | — |
| `include` | query | `string` | no | — |
| `fields[invoices]` | query | `string` | no | — |
| `fields[transactions]` | query | `string` | no | Optional fields transactions query parameter. |
| `fields[productionDays]` | query | `string` | no | Optional fields production days query parameter. |
| `fields[products]` | query | `string` | no | Optional fields products query parameter. |
