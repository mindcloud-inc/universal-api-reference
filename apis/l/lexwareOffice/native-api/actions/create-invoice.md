# Create Invoice with Lexware Office

Creates a new invoice in Lexware Office.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/invoices`
- **Base URL:** `https://api.lexware.io`
- **Official documentation:** [Create Invoice](https://developers.lexware.io/docs/#invoices-endpoint-create-an-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `voucherDate` | body | `date` | yes | RFC 3339 timestamp for the invoice date. |
| `address` | body | `object` | yes | JSON object for the invoice recipient address. |
| `lineItems[]` | body | `array<object>` | yes | JSON array of invoice line item objects. |
| `totalPrice` | body | `object` | yes | JSON object for the invoice total price. |
| `taxConditions` | body | `object` | yes | JSON object describing invoice tax conditions. |
| `shippingConditions` | body | `object` | yes | JSON object describing invoice shipping conditions. |
| `finalize` | query | `boolean` | no | Set to true to create an open invoice instead of the default draft invoice. |
