# Create Vendor Card with BILL Spend & Expense

Creates a new vendor card in BILL Spend & Expense.

## Endpoint

- **Method:** `POST`
- **Path:** `spend/cards`
- **Base URL:** `https://gateway.{environment}.bill.com/connect/v3`
- **Official documentation:** [Create Vendor Card](https://developer.bill.com/reference/createbudgetcard)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `expirationDate` | body | `string` | no | User-generated expiration date in yyyy-MM-dd format. |
| `name` | body | `string` | yes | Card name. |
| `budgetId` | body | `list` | yes | BILL-generated ID or UUID of the budget assigned to the card. |
| `userId` | body | `list` | yes | BILL-generated ID or UUID of the user assigned to the card. |
| `shareBudgetFunds` | body | `boolean` | no | Set true to share all budget funds with the card. |
| `limit` | body | `number` | no | Card spend limit for the current budget period. Required unless share budget funds is enabled. |
| `recurringLimit` | body | `number` | no | Card spend limit for all future budget periods when the assigned budget is recurring. |
