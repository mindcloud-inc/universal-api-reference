# Create Invoice Payment with Clockify

Creates a new invoice payment in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/invoices/:invoiceId/payments`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Create Invoice Payment](https://docs.developer.clockify.me/#tag/Invoice/operation/createInvoicePayment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `invoiceId` | path | `string<string>` | yes | — |
| `amount` | body | `number` | no | — |
| `note` | body | `string` | no | Maximum length: 1000. |
| `paymentDate` | body | `string` | no | — |
