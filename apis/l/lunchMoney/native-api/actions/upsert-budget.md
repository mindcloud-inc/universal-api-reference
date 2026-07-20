# Upsert budget with Lunch Money

## Endpoint

- **Method:** `PUT`
- **Path:** `/budgets`
- **Base URL:** `https://api.lunchmoney.dev/v2`
- **Official documentation:** [Upsert budget](https://alpha.lunchmoney.dev/v2/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `start_date` | body | `string` | yes |
| `category_id` | body | `number` | yes |
| `amount` | body | `number` | yes |
| `notes` | body | `string` | no |
