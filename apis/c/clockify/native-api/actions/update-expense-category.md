# Update Expense Category with Clockify

Updates an existing expense category in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/expenses/categories/:categoryId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Expense Category](https://docs.developer.clockify.me/#tag/Expense/operation/updateCategory)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `categoryId` | path | `string<string>` | yes | — |
| `name` | body | `string` | yes | Maximum length: 250. |
| `hasUnitPrice` | body | `boolean` | no | — |
| `priceInCents` | body | `number` | no | — |
| `unit` | body | `string` | no | — |
