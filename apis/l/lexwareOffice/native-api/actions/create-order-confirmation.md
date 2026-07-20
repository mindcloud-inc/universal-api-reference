# Create Order Confirmation with Lexware Office

Creates a new order confirmation in Lexware Office.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/order-confirmations`
- **Base URL:** `https://api.lexware.io`
- **Official documentation:** [Create Order Confirmation](https://developers.lexware.io/docs/#order-confirmations-endpoint-create-an-order-confirmation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `voucherDate` | body | `date` | yes | RFC 3339 timestamp for the order confirmation date. |
| `address` | body | `object` | yes | JSON object for the order confirmation recipient address. |
| `lineItems[]` | body | `array<object>` | yes | JSON array of order confirmation line item objects. |
| `totalPrice` | body | `object` | yes | JSON object for the order confirmation total price. |
| `taxConditions` | body | `object` | yes | JSON object describing order confirmation tax conditions. |
| `shippingConditions` | body | `object` | yes | JSON object describing order confirmation shipping conditions. |
| `finalize` | query | `boolean` | no | Set to true to create an open order confirmation instead of the default draft order confirmation. |
