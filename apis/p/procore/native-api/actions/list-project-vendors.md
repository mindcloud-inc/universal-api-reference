# List Project Vendors with Procore

Retrieves project vendors from Procore.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v1.1/projects/[:project_id]/vendors`
- **Base URL:** `https://api.procore.com`
- **Official documentation:** [List Project Vendors](https://developers.procore.com/reference/rest/project-vendors#list-project-vendors)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page` | query | `string` | no |
| `per_page` | query | `string` | no |
| `project_id` | path | `string` | no |
