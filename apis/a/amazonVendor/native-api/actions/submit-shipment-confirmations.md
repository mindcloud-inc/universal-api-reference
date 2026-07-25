# Submit Shipment Confirmations with Amazon Vendor

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/shipping/v1/shipmentConfirmations`
- **Base URL:** `https://sellingpartnerapi-{region}.amazon.com`
- **Official documentation:** [Submit Shipment Confirmations](https://developer-docs.amazon.com/sp-api/reference/submitshipmentconfirmations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shipmentConfirmations[]` | body | `array<object>` | yes | A list of one or more shipment confirmations. |
