# Get Expense with Clockify

Retrieves a specific expense from Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/expenses/:expenseId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Get Expense](https://docs.developer.clockify.me/#tag/Expense/operation/getExpense)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `expenseId` | path | `string<string>` | yes |
