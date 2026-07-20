# Create Project with Hubflo

Creates a new project in Hubflo.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://app.hubflo.com/api/v2`
- **Official documentation:** [Create Project](https://hubflo.readme.io/reference/post_api-v2-projects)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `estimated_revenue_amount` | body | `number` | no |
| `start_date` | body | `string` | no |
| `end_date` | body | `string` | no |
| `owner_id` | body | `string` | no |
| `owner_email` | body | `string` | no |
| `stage_id` | body | `string` | no |
| `primary_contact_id` | body | `string` | no |
| `address` | body | `string` | no |
| `workspace_id` | body | `string` | no |
| `tags` | body | `list<string>` | no |
| `user_ids` | body | `list<string>` | no |
