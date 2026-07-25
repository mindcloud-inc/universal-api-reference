# Submit Direct Fulfillment Shipment Confirmations with Amazon Vendor

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/directFulfillment/shipping/v1/shipmentConfirmations`
- **Base URL:** `https://sellingpartnerapi-{region}.amazon.com`
- **Official documentation:** [Submit Direct Fulfillment Shipment Confirmations](https://developer-docs.amazon.com/sp-api/reference/submitshipmentconfirmations-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shipmentConfirmations[]` | body | `array<object>` | yes | Array of direct fulfillment shipment confirmation objects. |
