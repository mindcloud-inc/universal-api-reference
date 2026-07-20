# Update Expense with Harpoon

Updates an existing expense in Harpoon.

## Endpoint

- **Method:** `PUT`
- **Path:** `/expenses/:id`
- **Base URL:** `https://app.harpoonapp.com/api`
- **Official documentation:** [Update Expense](https://app.harpoonapp.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `date` | body | `date` | no |
| `amount` | body | `number` | no |
| `vendor` | body | `string` | no |
| `description` | body | `string` | no |
| `expense_category_id` | body | `number` | no |
| `project_id` | body | `number` | no |
| `client_id` | body | `number` | no |
| `status` | body | `string` | no |
