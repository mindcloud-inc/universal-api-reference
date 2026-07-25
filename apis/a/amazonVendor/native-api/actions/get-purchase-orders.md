# Get Purchase Orders with Amazon Vendor

## Endpoint

- **Method:** `GET`
- **Path:** `/vendor/orders/v1/purchaseOrders`
- **Base URL:** `https://sellingpartnerapi-{region}.amazon.com`
- **Official documentation:** [Get Purchase Orders](https://developer-docs.amazon.com/sp-api/reference/getpurchaseorders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `createdAfter` | query | `date` | no | Purchase orders that became available after this ISO-8601 timestamp. |
| `createdBefore` | query | `date` | no | Purchase orders that became available before this ISO-8601 timestamp. |
| `changedAfter` | query | `date` | no | Purchase orders that changed after this ISO-8601 timestamp. |
| `changedBefore` | query | `date` | no | Purchase orders that changed before this ISO-8601 timestamp. |
| `sortOrder` | query | `list` | no | Sort ascending or descending by purchase order creation date. Accepted values: `ASC`, `DESC`. |
| `includeDetails` | query | `boolean` | no | When true, returns purchase orders with complete details. Otherwise, only purchase order numbers are returned. Format: `toggle`. |
| `poItemState` | query | `list` | no | Current state of the purchase order item. Amazon documents Cancelled as the allowed value. Accepted values: `Cancelled`. |
| `isPOChanged` | query | `boolean` | no | When true, returns purchase orders modified after placement. |
| `purchaseOrderState` | query | `list` | no | Filters purchase orders by purchase order state. Accepted values: `Acknowledged`, `Closed`, `New`. |
| `orderingVendorCode` | query | `string` | no | Filters purchase orders by ordering vendor code matching sellingParty.partyId. |
