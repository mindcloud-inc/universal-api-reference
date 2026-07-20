# Update Recurring Invoice with Invoice Ninja

## Endpoint

- **Method:** `PUT`
- **Path:** `/recurring_invoices/:id`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Update Recurring Invoice](https://api-docs.invoicing.co/#tag/Recurring-Invoices/operation/updateRecurringInvoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The recurring invoice identifier. |
| `private_notes` | body | `string` | no | Internal recurring invoice notes. |
| `remaining_cycles` | body | `string` | no | Updated remaining cycle count. |
| `due_date` | body | `string` | no | Updated due date. |
