# Update Bank Account with Column

## Endpoint

- **Method:** `PATCH`
- **Path:** `/bank-accounts/:bank_account_id`
- **Base URL:** `https://api.column.com`
- **Official documentation:** [Update Bank Account](https://column.com/docs/api/#bank-account/update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `bank_account_id` | path | `string` | yes |
| `description` | body | `string` | no |
| `display_name` | body | `string` | no |
| `is_interest_bearing` | body | `boolean` | no |
| `interest_config_id` | body | `string` | no |
| `is_overdraftable` | body | `boolean` | no |
| `overdraft_reserve_account_id` | body | `string` | no |
