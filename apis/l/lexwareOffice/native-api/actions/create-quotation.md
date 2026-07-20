# Create Quotation with Lexware Office

Creates a new quotation in Lexware Office.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/quotations`
- **Base URL:** `https://api.lexware.io`
- **Official documentation:** [Create Quotation](https://developers.lexware.io/docs/#quotations-endpoint-create-a-quotation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `voucherDate` | body | `date` | yes | RFC 3339 timestamp for the quotation date. |
| `expirationDate` | body | `date` | yes | RFC 3339 timestamp for the quotation expiration date. |
| `address` | body | `object` | yes | JSON object for the quotation recipient address. |
| `lineItems[]` | body | `array<object>` | yes | JSON array of quotation line item objects. |
| `totalPrice` | body | `object` | yes | JSON object for the quotation total price. |
| `taxConditions` | body | `object` | yes | JSON object describing quotation tax conditions. |
| `finalize` | query | `boolean` | no | Set to true to create an open quotation instead of the default draft quotation. |
