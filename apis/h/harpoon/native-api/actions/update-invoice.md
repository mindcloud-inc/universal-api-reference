# Update Invoice with Harpoon

Updates an existing invoice in Harpoon.

## Endpoint

- **Method:** `PUT`
- **Path:** `/invoices/:id`
- **Base URL:** `https://app.harpoonapp.com/api`
- **Official documentation:** [Update Invoice](https://app.harpoonapp.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `client_id` | body | `number` | no |
| `project_id` | body | `number` | no |
| `document_id` | body | `string` | no |
| `issue_date` | body | `date` | no |
| `due_date` | body | `date` | no |
| `status` | body | `string` | no |
| `discount` | body | `number` | no |
| `shipping` | body | `number` | no |
| `line_items[]` | body | `array<object>` | no |
