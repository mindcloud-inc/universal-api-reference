# Create Expense with FreeAgent

Creates a new expense in FreeAgent.

## Endpoint

- **Method:** `POST`
- **Path:** `/expenses`
- **Base URL:** `https://api.freeagent.com/v2`
- **Official documentation:** [Create Expense](https://dev.freeagent.com/docs/expenses#create-an-expense)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `expense` | body | `object` | no | Expense payload. |
| `expense.user` | body | `string` | yes | Expense claimant. |
| `expense.category` | body | `string` | yes | Expense category. |
| `expense.dated_on` | body | `date` | yes | Date of expense in YYYY-MM-DD format. |
| `expense.description` | body | `string` | yes | Free-text description. |
| `expense.gross_value` | body | `number` | no | Total value expressed in the given currency. |
| `expense.currency` | body | `string` | no | Expense currency. |
| `expense.sales_tax_status` | body | `string` | no | Sales tax status. |
| `expense.project` | body | `string` | no | Project to rebill. |
