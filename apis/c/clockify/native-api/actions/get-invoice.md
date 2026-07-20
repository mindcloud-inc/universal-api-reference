# Get Invoice with Clockify

Retrieves a specific invoice from Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/invoices/:invoiceId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Get Invoice](https://docs.developer.clockify.me/#tag/Invoice/operation/getInvoice)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `invoiceId` | path | `string<string>` | yes |
