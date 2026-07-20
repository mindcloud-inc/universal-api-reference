# Create User with BILL Spend & Expense

Creates a new user in BILL Spend & Expense.

## Endpoint

- **Method:** `POST`
- **Path:** `spend/users`
- **Base URL:** `https://gateway.{environment}.bill.com/connect/v3`
- **Official documentation:** [Create User](https://developer.bill.com/reference/createuser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | User email address. |
| `firstName` | body | `string` | yes | User first name. |
| `lastName` | body | `string` | yes | User last name. |
| `role` | body | `list<string>` | yes | User role. |
