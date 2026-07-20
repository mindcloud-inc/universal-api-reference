# Update Category with EnvelopeBudget

## Endpoint

- **Method:** `PATCH`
- **Path:** `/categories/:budget_id/:category_id`
- **Base URL:** `https://envelopebudget.com/api`
- **Official documentation:** [Update Category](https://envelopebudget.com/api/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `budget_id` | path | `string` | yes |
| `category_id` | path | `string` | yes |
| `name` | body | `string` | no |
