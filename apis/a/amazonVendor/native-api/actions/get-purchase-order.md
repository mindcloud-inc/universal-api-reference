# Get Purchase Order with Amazon Vendor

## Endpoint

- **Method:** `GET`
- **Path:** `/vendor/orders/v1/purchaseOrders/:purchaseOrderNumber`
- **Base URL:** `https://sellingpartnerapi-{region}.amazon.com`
- **Official documentation:** [Get Purchase Order](https://developer-docs.amazon.com/sp-api/reference/getpurchaseorder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `purchaseOrderNumber` | path | `string` | yes | The 8-character alphanumeric purchase order identifier. |
