# Create Direct Fulfillment Shipping Labels with Amazon Vendor

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/directFulfillment/shipping/2021-12-28/shippingLabels/:purchaseOrderNumber`
- **Base URL:** `https://sellingpartnerapi-{region}.amazon.com`
- **Official documentation:** [Create Direct Fulfillment Shipping Labels](https://developer-docs.amazon.com/sp-api/reference/createshippinglabels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `purchaseOrderNumber` | path | `string` | yes | Amazon purchase order number for the Direct Fulfillment shipping label request. |
| `sellingParty` | body | `object` | yes | Selling party information for the Direct Fulfillment shipping label request. |
| `shipFromParty` | body | `object` | yes | Ship-from party information for the Direct Fulfillment shipping label request. |
| `containers[]` | body | `array<object>` | no | Container details for the Direct Fulfillment shipping label request. |
