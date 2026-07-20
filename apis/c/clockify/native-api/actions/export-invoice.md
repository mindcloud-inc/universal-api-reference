# Export Invoice with Clockify

Exports a workspace invoice from Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/invoices/:invoiceId/export`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Export Invoice](https://docs.developer.clockify.me/#tag/Invoice/operation/exportInvoice)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `invoiceId` | path | `string<string>` | yes |
| `userLocale` | query | `string` | yes |
