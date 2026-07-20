# Create Budget with BILL Spend & Expense

Creates a new budget in BILL Spend & Expense.

## Endpoint

- **Method:** `POST`
- **Path:** `spend/budgets`
- **Base URL:** `https://gateway.{environment}.bill.com/connect/v3`
- **Official documentation:** [Create Budget](https://developer.bill.com/reference/createbudget)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Budget description. |
| `name` | body | `string` | yes | Budget name. |
| `owners[]` | body | `array<string>` | yes | List of BILL-generated user IDs or UUIDs of budget owners. You must specify at least one budget owner. |
| `recurringInterval` | body | `list` | yes | Interval after which the budget is reset. Accepted values: `DAILY`, `MONTHLY`, `NONE`, `QUARTERLY`, `WEEKLY`, `YEARLY`. |
| `limit` | body | `number` | yes | Spend limit for the initial budget period. Required unless limitless overspend is enabled. |
| `recurringLimit` | body | `number` | no | Spend limit for all future budget periods. Required when recurring interval is not NONE. |
