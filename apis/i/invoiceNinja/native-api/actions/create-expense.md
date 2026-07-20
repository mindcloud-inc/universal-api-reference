# Create Expense with Invoice Ninja

## Endpoint

- **Method:** `POST`
- **Path:** `/expenses`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Create Expense](https://api-docs.invoicing.co/#tag/expenses/operation/storeExpense)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vendor_id` | body | `string` | no | The vendor for the expense. |
| `amount` | body | `number` | no | Expense amount. |
| `date` | body | `string` | no | Expense date. |
| `private_notes` | body | `string` | no | Internal expense notes. |
| `public_notes` | body | `string` | no | Expense description visible on documents. |
