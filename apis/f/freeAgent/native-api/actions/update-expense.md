# Update Expense with FreeAgent

Updates an existing expense in FreeAgent.

## Endpoint

- **Method:** `PUT`
- **Path:** `/expenses/:id`
- **Base URL:** `https://api.freeagent.com/v2`
- **Official documentation:** [Update Expense](https://dev.freeagent.com/docs/expenses#update-an-expense)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | FreeAgent expense ID. |
| `expense` | body | `object` | no | Expense payload. |
| `expense.user` | body | `string` | no | Expense claimant. |
| `expense.category` | body | `string` | no | Expense category. |
| `expense.dated_on` | body | `date` | no | Date of expense in YYYY-MM-DD format. |
| `expense.description` | body | `string` | no | Free-text description. |
| `expense.gross_value` | body | `number` | no | Total value expressed in the given currency. |
| `expense.currency` | body | `string` | no | Expense currency. |
| `expense.sales_tax_status` | body | `string` | no | Sales tax status. |
| `expense.project` | body | `string` | no | Project to rebill. |
