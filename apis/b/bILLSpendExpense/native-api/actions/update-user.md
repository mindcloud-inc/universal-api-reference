# Update User with BILL Spend & Expense

Updates an existing user in BILL Spend & Expense.

## Endpoint

- **Method:** `PATCH`
- **Path:** `spend/users/:userId`
- **Base URL:** `https://gateway.{environment}.bill.com/connect/v3`
- **Official documentation:** [Update User](https://developer.bill.com/reference/updateuser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateOfBirth` | body | `date` | no | User date of birth in yyyy-MM-dd format. |
| `email` | body | `string` | no | User email address. |
| `firstName` | body | `string` | no | User first name. |
| `lastName` | body | `string` | no | User last name. |
| `role` | body | `string` | no | User role. |
| `userId` | path | `list` | yes | BILL-generated ID or UUID of the user. |
