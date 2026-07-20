# Create Invoice with Clockify

Creates a new invoice in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/invoices`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Create Invoice](https://docs.developer.clockify.me/#tag/Invoice/operation/createInvoice)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `clientId` | body | `list<string>` | yes |
| `currency` | body | `string` | yes |
| `dueDate` | body | `date` | yes |
| `issuedDate` | body | `date` | yes |
| `number` | body | `string` | yes |
