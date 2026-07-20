# Update Expense with Clockify

Updates an existing expense in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/expenses/:expenseId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Expense](https://docs.developer.clockify.me/#tag/Expense/operation/updateExpense)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `expenseId` | path | `string<string>` | yes |
| `amount` | body | `number` | yes |
| `categoryId` | body | `list<string>` | yes |
| `changeFields[]` | body | `array<string>` | yes |
| `date` | body | `date` | yes |
| `file` | body | `file` | yes |
| `userId` | body | `list<string>` | yes |
| `billable` | body | `boolean` | no |
| `notes` | body | `string` | no |
| `projectId` | body | `list<string>` | no |
| `taskId` | body | `list<string>` | no |
