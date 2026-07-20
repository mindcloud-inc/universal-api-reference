# Get Expense with FreshBooks

Retrieves an expense from FreshBooks for an account.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounting/account/:accountId/expenses/expenses/:expenseId`
- **Base URL:** `https://api.freshbooks.com`
- **Official documentation:** [Get Expense](https://www.freshbooks.com/api/expenses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | FreshBooks accounting account ID. |
| `expenseId` | path | `string` | yes | FreshBooks expense ID. |
