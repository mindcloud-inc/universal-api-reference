# List Workspace Expenses with Clockify

Lists all workspace expenses in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/expenses`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [List Workspace Expenses](https://docs.developer.clockify.me/#tag/Expense/operation/getExpenses)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `user-id` | query | `list<string>` | no |
