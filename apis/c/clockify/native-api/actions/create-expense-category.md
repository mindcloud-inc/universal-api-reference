# Create Expense Category with Clockify

Creates a new expense category in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/expenses/categories`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Create Expense Category](https://docs.developer.clockify.me/#tag/Expense/operation/createExpenseCategory)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `name` | body | `string` | yes | Maximum length: 250. |
| `hasUnitPrice` | body | `boolean` | no | — |
| `priceInCents` | body | `number` | no | — |
| `unit` | body | `string` | no | — |
