# Update Project with Hubflo

Updates an existing project in Hubflo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:id`
- **Base URL:** `https://app.hubflo.com/api/v2`
- **Official documentation:** [Update Project](https://hubflo.readme.io/reference/patch_api-v2-projects-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
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
