# Delete Expense Category with Clockify

Deletes an existing expense category from Clockify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `workspaces/:workspaceId/expenses/categories/:categoryId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Delete Expense Category](https://docs.developer.clockify.me/#tag/Expense/operation/deleteCategory)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `categoryId` | path | `string<string>` | yes |
