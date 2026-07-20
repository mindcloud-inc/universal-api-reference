# List Workspace Invoices with Clockify

Lists all workspace invoices in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/invoices`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [List Workspace Invoices](https://docs.developer.clockify.me/#tag/Invoice/operation/getInvoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `statuses` | query | `list<string>` | no | Accepted values: `OVERDUE`, `PAID`, `PARTIALLY_PAID`, `SENT`, `UNSENT`, `VOID`. |
