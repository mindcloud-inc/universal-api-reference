# Create Account Number with Column

## Endpoint

- **Method:** `POST`
- **Path:** `/bank-accounts/:bank_account_id/account-numbers`
- **Base URL:** `https://api.column.com`
- **Official documentation:** [Create Account Number](https://column.com/docs/api/#account-number/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `bank_account_id` | path | `string` | yes |
| `description` | body | `string` | no |
