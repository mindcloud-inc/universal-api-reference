# Delete Invoice with Clockify

Deletes an existing invoice from Clockify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `workspaces/:workspaceId/invoices/:invoiceId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Delete Invoice](https://docs.developer.clockify.me/#tag/Invoice/operation/deleteInvoice)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `invoiceId` | path | `string<string>` | yes |
