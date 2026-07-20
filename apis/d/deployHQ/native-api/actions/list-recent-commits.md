# List Recent Commits with DeployHQ

Retrieves recent repository commits from DeployHQ.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/repository/recent_commits`
- **Base URL:** `https://{account}.deployhq.com`
- **Official documentation:** [List Recent Commits](https://api.deployhq.com/docs#tag/Repositories/operation/recentCommitsProjectRepository)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The identifier or permalink of the project. |
| `branch` | query | `string` | no | The branch name to get recent commits for. |
| `update` | query | `boolean` | no | Set to 1 to update the repository before getting recent commits. |
