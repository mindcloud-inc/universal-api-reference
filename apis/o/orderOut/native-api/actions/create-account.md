# Create Account with OrderOut

Creates an account in OrderOut.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/pos/account`
- **Base URL:** `https://api.orderout.co`
- **Official documentation:** [Create Account](https://developers.orderout.co/reference/create-account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_manager_email` | body | `string` | yes | Account manager email |
| `account_manager_firstname` | body | `string` | yes | Account manager first name |
| `account_manager_lastname` | body | `string` | yes | Account manager last name |
| `account_manager_phone` | body | `string` | yes | Account manager phone |
| `account_name` | body | `string` | yes | Account name |
