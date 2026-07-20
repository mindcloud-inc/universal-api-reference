# Create Estimate with Harpoon

Creates a new estimate in Harpoon.

## Endpoint

- **Method:** `POST`
- **Path:** `/estimates`
- **Base URL:** `https://app.harpoonapp.com/api`
- **Official documentation:** [Create Estimate](https://app.harpoonapp.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `client_id` | body | `number` | no |
| `project_id` | body | `number` | no |
| `document_id` | body | `string` | no |
| `issue_date` | body | `date` | no |
| `due_date` | body | `date` | no |
| `subject` | body | `string` | no |
| `note` | body | `string` | no |
| `line_items[]` | body | `array<object>` | no |
