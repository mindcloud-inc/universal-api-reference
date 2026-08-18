# Update Invoice with Centerpoint

## Endpoint

- **Method:** `PATCH`
- **Path:** `invoices/:INVOICE_ID`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [Update Invoice](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/invoices/{INVOICE_ID}PATCH)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.attributes` | body | `object` | no |
| `data.attributes.status` | body | `string` | no |
| `INVOICE_ID` | path | `string` | yes |
| `data` | body | `object` | no |
| `data.type` | body | `string` | no |
| `data.id` | body | `string` | no |
