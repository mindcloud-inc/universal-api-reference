# List Production Purchase Orders with Centerpoint

## Endpoint

- **Method:** `GET`
- **Path:** `productions/:PRODUCTION_ID/purchase_orders`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [List Production Purchase Orders](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/productions/{PRODUCTION_ID}/purchase_ordersGET)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PRODUCTION_ID` | path | `string` | yes | The production id to retrieve. |
| `fields[profiles]` | query | `string` | no | Optional fields profiles query parameter. |
| `fields[employees]` | query | `string` | no | Optional fields employees query parameter. |
| `include` | query | `string` | no | Optional include query parameter. |
