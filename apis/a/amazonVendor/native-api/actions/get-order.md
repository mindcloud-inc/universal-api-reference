# Get Order with Amazon Vendor

## Endpoint

- **Method:** `GET`
- **Path:** `/vendor/directFulfillment/orders/2021-12-28/purchaseOrders/:purchaseOrderNumber`
- **Base URL:** `https://sellingpartnerapi-{region}.amazon.com`
- **Official documentation:** [Get Order](https://developer-docs.amazon.com/sp-api/reference/getorder-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `purchaseOrderNumber` | path | `string` | yes | The alphanumeric identifier of the purchase order to retrieve. |
