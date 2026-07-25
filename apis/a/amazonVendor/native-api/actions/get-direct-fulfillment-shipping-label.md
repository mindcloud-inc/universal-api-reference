# Get Direct Fulfillment Shipping Label with Amazon Vendor

## Endpoint

- **Method:** `GET`
- **Path:** `/vendor/directFulfillment/shipping/2021-12-28/shippingLabels/:purchaseOrderNumber`
- **Base URL:** `https://sellingpartnerapi-{region}.amazon.com`
- **Official documentation:** [Get Direct Fulfillment Shipping Label](https://developer-docs.amazon.com/sp-api/reference/getshippinglabel-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `purchaseOrderNumber` | path | `string` | yes | Amazon purchase order number for the Direct Fulfillment shipping label to retrieve. |
