# Update Project with Felt

Updates an existing project in Felt.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/update`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Update Project](https://developers.felt.com/rest-api/api-reference/projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The Felt project ID. |
| `name` | body | `string` | no | The new project name. |
| `visibility` | body | `string` | no | Project visibility: workspace or private. |
| `max_inherited_permission` | body | `string` | no | Maximum permission inherited by workspace members for workspace-visible projects. |
