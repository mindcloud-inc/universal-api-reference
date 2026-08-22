# Get Direct Fulfillment Packing Slip with Amazon Vendor

## Endpoint

- **Method:** `GET`
- **Path:** `/vendor/directFulfillment/shipping/2021-12-28/packingSlips/:purchaseOrderNumber`
- **Base URL:** `https://sellingpartnerapi-{region}.amazon.com`
- **Official documentation:** [Get Direct Fulfillment Packing Slip](https://developer-docs.amazon.com/sp-api/reference/getpackingslip-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `purchaseOrderNumber` | path | `string` | yes | The purchaseOrderNumber for the packing slip that you want. |
