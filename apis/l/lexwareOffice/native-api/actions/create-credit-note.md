# Create Credit Note with Lexware Office

Creates a new credit note in Lexware Office.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/credit-notes`
- **Base URL:** `https://api.lexware.io`
- **Official documentation:** [Create Credit Note](https://developers.lexware.io/docs/#credit-notes-endpoint-create-a-credit-note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `voucherDate` | body | `date` | yes | RFC 3339 timestamp for the credit note date. |
| `address` | body | `object` | yes | JSON object for the credit note recipient address. |
| `lineItems[]` | body | `array<object>` | yes | JSON array of credit note line item objects. |
| `totalPrice` | body | `object` | yes | JSON object for the credit note total price. |
| `taxConditions` | body | `object` | yes | JSON object describing credit note tax conditions. |
| `finalize` | query | `boolean` | no | Set to true to create an open credit note instead of the default draft credit note. |
