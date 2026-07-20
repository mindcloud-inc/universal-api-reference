# Create Bank Account with Column

## Endpoint

- **Method:** `POST`
- **Path:** `/bank-accounts`
- **Base URL:** `https://api.column.com`
- **Official documentation:** [Create Bank Account](https://column.com/docs/api/#bank-account/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `description` | body | `string` | yes |
| `entity_id` | body | `string` | yes |
| `display_name` | body | `string` | no |
| `is_interest_bearing` | body | `boolean` | no |
| `interest_config_id` | body | `string` | no |
| `is_overdraftable` | body | `boolean` | no |
| `overdraft_reserve_account_id` | body | `string` | no |
