# Duplicate Invoice with Clockify

Duplicates an existing invoice in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/invoices/:invoiceId/duplicate`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Duplicate Invoice](https://docs.developer.clockify.me/#tag/Invoice/operation/duplicateInvoice)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `invoiceId` | path | `string<string>` | yes |
