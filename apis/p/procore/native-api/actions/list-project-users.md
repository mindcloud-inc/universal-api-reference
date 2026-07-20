# List Project Users with Procore

Retrieves project users from Procore.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v1.0/projects/[:project_id]/users`
- **Base URL:** `https://api.procore.com`
- **Official documentation:** [List Project Users](https://developers.procore.com/reference/rest/project-users#list-project-users)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page` | query | `string` | no |
| `per_page` | query | `string` | no |
| `project_id` | path | `string` | no |
