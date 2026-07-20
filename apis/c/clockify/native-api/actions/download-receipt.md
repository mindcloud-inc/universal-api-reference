# Download Receipt with Clockify

Downloads an expense receipt from Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/expenses/:expenseId/files/:fileId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Download Receipt](https://docs.developer.clockify.me/#tag/Expense/operation/downloadFile)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `expenseId` | path | `string<string>` | yes |
| `fileId` | path | `string` | yes |
