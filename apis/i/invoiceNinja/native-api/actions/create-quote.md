# Create Quote with Invoice Ninja

## Endpoint

- **Method:** `POST`
- **Path:** `/quotes`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Create Quote](https://api-docs.invoicing.co/#tag/quotes/operation/storeQuote)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | body | `string` | yes | Hashed client ID for the quote. |
| `date` | body | `string` | yes | Quote date in YYYY-MM-DD format. |
| `due_date` | body | `string` | yes | Quote due date in YYYY-MM-DD format. |
| `public_notes` | body | `string` | no | Public notes for the quote. |
| `line_items[0].product_key` | body | `string` | yes | Product key for the first line item. |
| `line_items[0].quantity` | body | `number` | yes | Quantity for the first line item. |
| `line_items[0].cost` | body | `number` | yes | Cost for the first line item. |
