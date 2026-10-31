# Delete Project Task Role with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/tasks/:taskId/roles/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Project Task Role](https://developers.gobridgit.com/reference/projecttasks_removerole)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The project ID that the task belongs to |
| `taskId` | path | `string` | yes | The task ID that the role belongs to |
| `id` | path | `number` | yes | The role ID |
