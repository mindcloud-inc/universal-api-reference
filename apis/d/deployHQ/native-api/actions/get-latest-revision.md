# Get Latest Revision with DeployHQ

Retrieves the latest repository revision from DeployHQ.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/repository/latest_revision`
- **Base URL:** `https://{account}.deployhq.com`
- **Official documentation:** [Get Latest Revision](https://api.deployhq.com/docs#tag/Repositories/operation/latestRevisionProjectRepository)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The identifier or permalink of the project. |
| `branch` | query | `string` | no | The branch name to get the latest revision for. |
| `update` | query | `boolean` | no | Set to 1 to update the repository before getting the latest revision. |
