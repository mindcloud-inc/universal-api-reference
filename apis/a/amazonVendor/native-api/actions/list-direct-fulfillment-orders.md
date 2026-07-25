# List Direct Fulfillment Orders with Amazon Vendor

## Endpoint

- **Method:** `GET`
- **Path:** `/vendor/directFulfillment/orders/2021-12-28/purchaseOrders`
- **Base URL:** `https://sellingpartnerapi-{region}.amazon.com`
- **Official documentation:** [List Direct Fulfillment Orders](https://developer-docs.amazon.com/sp-api/reference/getorders-2)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `createdAfter` | query | `date` | yes | Purchase orders that became available after this ISO-8601 date/time. |
| `createdBefore` | query | `date` | yes | Purchase orders that became available before this ISO-8601 date/time. |
| `shipFromPartyId` | query | `string` | no | Vendor warehouse identifier for the fulfillment warehouse. |
| `status` | query | `list` | no | Purchase order status to return. Accepted values: `Accepted`, `Cancelled`, `New`, `Shipped`. |
| `sortOrder` | query | `list` | no | Sort order by order creation date. Accepted values: `Ascending`, `Descending`. |
| `includeDetails` | query | `string` | no | When true, returns complete purchase order details; otherwise only purchase order numbers. |
