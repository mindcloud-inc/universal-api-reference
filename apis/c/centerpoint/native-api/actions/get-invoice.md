# Get Invoice with Centerpoint

## Endpoint

- **Method:** `GET`
- **Path:** `invoices/:invoice_id`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [Get Invoice](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/invoices/{INVOICE_ID}GET)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `invoice_id` | path | `string` | yes |
| `include` | query | `string` | no |
| `fields[invoices]` | query | `string` | no |
