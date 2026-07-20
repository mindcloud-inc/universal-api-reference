# Delete Expense with Clockify

Deletes an existing expense from Clockify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `workspaces/:workspaceId/expenses/:expenseId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Delete Expense](https://docs.developer.clockify.me/#tag/Expense/operation/deleteExpense)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `expenseId` | path | `string<string>` | yes |
