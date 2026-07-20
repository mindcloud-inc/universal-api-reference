# Create Expense with Harpoon

Creates a new expense in Harpoon.

## Endpoint

- **Method:** `POST`
- **Path:** `/expenses`
- **Base URL:** `https://app.harpoonapp.com/api`
- **Official documentation:** [Create Expense](https://app.harpoonapp.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `date` | body | `date` | no |
| `amount` | body | `number` | no |
| `vendor` | body | `string` | no |
| `description` | body | `string` | no |
| `expense_category_id` | body | `number` | no |
| `project_id` | body | `number` | no |
| `client_id` | body | `number` | no |
| `status` | body | `string` | no |
