# Update Project with Simplicate

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/project/:id`
- **Base URL:** `https://{subdomain}/api/v2`
- **Official documentation:** [Update Project](https://developer.simplicate.com/docs/api/v2/reference/update-projects-project/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The project id |
| `name` | body | `string` | no | The project name |
| `note` | body | `string` | no | A note for the project |
