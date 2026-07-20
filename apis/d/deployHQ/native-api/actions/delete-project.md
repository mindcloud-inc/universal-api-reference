# Delete Project with DeployHQ

Deletes an existing project from DeployHQ.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:id`
- **Base URL:** `https://{account}.deployhq.com`
- **Official documentation:** [Delete Project](https://api.deployhq.com/docs#tag/Projects/operation/deleteProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The identifier or permalink of the project. |
