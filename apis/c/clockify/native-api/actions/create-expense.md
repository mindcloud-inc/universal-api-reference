# Create Expense with Clockify

Creates a new expense in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/expenses`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Create Expense](https://docs.developer.clockify.me/#tag/Expense/operation/createExpense)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `amount` | body | `number` | yes |
| `categoryId` | body | `list<string>` | yes |
| `date` | body | `date` | yes |
| `file` | body | `file` | yes |
| `projectId` | body | `list<string>` | yes |
| `userId` | body | `list<string>` | yes |
| `billable` | body | `boolean` | no |
| `notes` | body | `string` | no |
| `taskId` | body | `list<string>` | no |
