# List Purchase Orders with Ramp

## Endpoint

- **Method:** `GET`
- **Path:** `transactions`
- **Base URL:** `https://api.ramp.com/developer/v1/`
- **Official documentation:** [List Purchase Orders](https://docs.ramp.com/developer-api/v1/api/transactions)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accounting_field_selection_id` | query | `string` | no |
| `approval_status` | query | `string` | no |
| `awaiting_approval_by_user_id` | query | `string` | no |
| `card_id` | query | `string` | no |
| `department_id` | query | `string` | no |
| `entity_id` | query | `string` | no |
| `from_date` | query | `string` | no |
| `has_no_sync_commits` | query | `boolean` | no |
| `include_merchant_data` | query | `boolean` | no |
| `limit_id` | query | `string` | no |
| `location_id` | query | `string` | no |
| `max_amount` | query | `number` | no |
| `merchant_id` | query | `string` | no |
| `min_amount` | query | `number` | no |
| `order_by_amount_asc` | query | `boolean` | no |
| `order_by_amount_desc` | query | `boolean` | no |
| `order_by_date_asc` | query | `boolean` | no |
| `order_by_date_desc` | query | `boolean` | no |
| `requires_memo` | query | `boolean` | no |
| `sk_category_id` | query | `string` | no |
| `spend_program_id` | query | `string` | no |
| `state` | query | `string` | no |
| `statement_id` | query | `string` | no |
| `sync_ready` | query | `boolean` | no |
| `sync_status` | query | `string` | no |
| `synced_after` | query | `string` | no |
| `to_date` | query | `string` | no |
| `trip_id` | query | `string` | no |
| `user_id` | query | `string` | no |
