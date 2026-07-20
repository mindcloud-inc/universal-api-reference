# List Expense Categories with Clockify

Lists all expense categories in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/expenses/categories`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [List Expense Categories](https://docs.developer.clockify.me/#tag/Expense/operation/getCategories)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `archived` | query | `boolean` | no |
| `name` | query | `string` | no |
