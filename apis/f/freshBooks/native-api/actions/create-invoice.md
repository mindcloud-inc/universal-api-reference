# Create Invoice with FreshBooks

Creates a new invoice in FreshBooks for an account.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounting/account/:accountId/invoices/invoices`
- **Base URL:** `https://api.freshbooks.com`
- **Official documentation:** [Create Invoice](https://www.freshbooks.com/api/invoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | FreshBooks accounting account ID. |
| `invoice.customerid` | body | `number` | yes | — |
| `invoice.create_date` | body | `string` | yes | — |
| `invoice.due_date` | body | `string` | no | — |
| `invoice.notes` | body | `string` | no | — |
| `invoice.lines[].name` | body | `string` | yes | — |
| `invoice.lines[].qty` | body | `number` | yes | — |
| `invoice.lines[].unit_cost.amount` | body | `string` | yes | — |
| `invoice.lines[].unit_cost.code` | body | `string` | yes | — |
