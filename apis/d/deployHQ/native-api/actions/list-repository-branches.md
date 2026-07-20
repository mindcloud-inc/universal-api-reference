# List Repository Branches with DeployHQ

Retrieves repository branches from DeployHQ.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/repository/branches`
- **Base URL:** `https://{account}.deployhq.com`
- **Official documentation:** [List Repository Branches](https://api.deployhq.com/docs#tag/Repositories/operation/branchesProjectRepository)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The identifier or permalink of the project. |
