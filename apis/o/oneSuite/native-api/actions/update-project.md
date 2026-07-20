# Update Project with OneSuite

Updates a project in OneSuite.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/projects/:project_id`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [Update Project](https://rest-api.onesuite.io/#edit-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The ID of the project to update |
| `name` | body | `string` | no | Updated project name |
| `client.key` | body | `string` | no | Client ID for the project |
