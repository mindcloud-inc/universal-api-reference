# Create Project with Felt

Creates a new project in Felt.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Create Project](https://developers.felt.com/rest-api/api-reference/projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Project name. |
| `visibility` | body | `string` | yes | Project visibility. Felt docs support workspace or private. |
| `max_inherited_permission` | body | `string` | no | Maximum permission workspace members inherit on workspace-visible projects. |
