# List Projects with Moco

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://{domain}.mocoapp.com/api/v1`
- **Official documentation:** [List Projects](https://everii-group.github.io/mocoapp-api-docs/sections/projects.html#get-projects)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company_id` | query | `string` | no |
| `created_from` | query | `date` | no |
| `created_to` | query | `date` | no |
| `custom_properties` | query | `object` | no |
| `deal_id` | query | `string` | no |
| `identifier` | query | `string` | no |
| `ids` | query | `string` | no |
| `include_archived` | query | `boolean` | no |
| `include_company` | query | `boolean` | no |
| `leader_id` | query | `string` | no |
| `project_group_id` | query | `string` | no |
| `retainer` | query | `boolean` | no |
| `tags` | query | `string` | no |
| `updated_after` | query | `date` | no |
| `updated_from` | query | `date` | no |
| `updated_to` | query | `date` | no |
