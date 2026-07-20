# Update Invoice with FreshBooks

Updates an existing invoice in FreshBooks for an account.

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounting/account/:accountId/invoices/invoices/:invoiceId`
- **Base URL:** `https://api.freshbooks.com`
- **Official documentation:** [Update Invoice](https://www.freshbooks.com/api/invoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | FreshBooks accounting account ID. |
| `invoiceId` | path | `string` | yes | FreshBooks invoice ID. |
| `invoice.customerid` | body | `number` | no | — |
| `invoice.create_date` | body | `string` | no | — |
| `invoice.due_date` | body | `string` | no | — |
| `invoice.notes` | body | `string` | no | — |
| `invoice.lines[].name` | body | `string` | no | — |
| `invoice.lines[].qty` | body | `number` | no | — |
| `invoice.lines[].unit_cost.amount` | body | `string` | no | — |
| `invoice.lines[].unit_cost.code` | body | `string` | no | — |
