# Change Invoice Status with Clockify

Updates an invoice status in Clockify.

## Endpoint

- **Method:** `PATCH`
- **Path:** `workspaces/:workspaceId/invoices/:invoiceId/status`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Change Invoice Status](https://docs.developer.clockify.me/#tag/Invoice/operation/changeInvoiceStatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `invoiceId` | path | `string<string>` | yes | — |
| `invoiceStatus` | body | `list<string>` | no | Accepted values: `OVERDUE`, `PAID`, `PARTIALLY_PAID`, `SENT`, `UNSENT`, `VOID`. |
