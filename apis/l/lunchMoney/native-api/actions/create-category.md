# Create a new category or category group with Lunch Money

## Endpoint

- **Method:** `POST`
- **Path:** `/categories`
- **Base URL:** `https://api.lunchmoney.dev/v2`
- **Official documentation:** [Create a new category or category group](https://alpha.lunchmoney.dev/v2/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `description` | body | `string` | no |
| `is_group` | body | `boolean` | no |
| `group_id` | body | `number` | no |
| `archived` | body | `boolean` | no |
