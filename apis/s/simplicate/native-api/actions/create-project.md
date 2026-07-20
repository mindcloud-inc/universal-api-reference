# Create Project with Simplicate

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/project`
- **Base URL:** `https://{subdomain}/api/v2`
- **Official documentation:** [Create Project](https://developer.simplicate.com/docs/api/v2/reference/create-projects-project/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `my_organization_profile_id` | body | `string` | no | The organization profile id for the project |
| `name` | body | `string` | no | The project name |
| `note` | body | `string` | no | A note for the project |
| `organization_id` | body | `string` | no | The organization id for the project |
| `project_status_id` | body | `string` | no | The project status id |
