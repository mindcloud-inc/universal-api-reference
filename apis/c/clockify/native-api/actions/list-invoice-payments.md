# List Invoice Payments with Clockify

Lists all invoice payments in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/invoices/:invoiceId/payments`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [List Invoice Payments](https://docs.developer.clockify.me/#tag/Invoice/operation/getPaymentsForInvoice)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `invoiceId` | path | `string<string>` | yes |
