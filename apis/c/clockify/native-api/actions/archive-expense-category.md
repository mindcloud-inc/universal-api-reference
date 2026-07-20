# Archive Expense Category with Clockify

Archives an expense category in Clockify.

## Endpoint

- **Method:** `PATCH`
- **Path:** `workspaces/:workspaceId/expenses/categories/:categoryId/status`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Archive Expense Category](https://docs.developer.clockify.me/#tag/Expense/operation/updateExpenseCategoryStatus)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `categoryId` | path | `string<string>` | yes |
| `archived` | body | `boolean` | no |
