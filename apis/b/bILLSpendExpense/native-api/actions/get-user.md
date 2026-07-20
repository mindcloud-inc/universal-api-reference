# Get User with BILL Spend & Expense

Retrieves a user from BILL Spend & Expense.

## Endpoint

- **Method:** `GET`
- **Path:** `spend/users/:userId`
- **Base URL:** `https://gateway.{environment}.bill.com/connect/v3`
- **Official documentation:** [Get User](https://developer.bill.com/reference/getuser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `list` | yes | BILL-generated ID or UUID of the user. |
