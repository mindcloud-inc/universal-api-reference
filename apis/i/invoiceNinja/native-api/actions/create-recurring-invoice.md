# Create Recurring Invoice with Invoice Ninja

## Endpoint

- **Method:** `POST`
- **Path:** `/recurring_invoices`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Create Recurring Invoice](https://api-docs.invoicing.co/#tag/Recurring-Invoices/operation/storeRecurringInvoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | body | `string` | yes | The client to bill. |
| `date` | body | `string` | yes | The recurring invoice date. |
| `due_date` | body | `string` | yes | The recurring invoice due date. |
| `frequency_id` | body | `string` | yes | The recurrence frequency. |
| `remaining_cycles` | body | `string` | no | Optional number of remaining cycles. |
| `private_notes` | body | `string` | no | Internal recurring invoice notes. |
| `line_items` | body | `list<object>` | no | Line items for the recurring invoice. |
