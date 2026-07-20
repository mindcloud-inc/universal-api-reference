# Get Repository with DeployHQ

Retrieves the repository for a project from DeployHQ.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/repository`
- **Base URL:** `https://{account}.deployhq.com`
- **Official documentation:** [Get Repository](https://api.deployhq.com/docs#tag/Repositories/operation/getProjectRepository)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The identifier or permalink of the project. |
