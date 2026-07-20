# Delete a manual account with Lunch Money

## Endpoint

- **Method:** `DELETE`
- **Path:** `/manual_accounts/:id`
- **Base URL:** `https://api.lunchmoney.dev/v2`
- **Official documentation:** [Delete a manual account](https://alpha.lunchmoney.dev/v2/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `delete_items` | query | `boolean` | no |
| `delete_balance_history` | query | `boolean` | no |
