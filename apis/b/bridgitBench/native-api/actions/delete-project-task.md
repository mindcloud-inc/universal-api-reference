# Delete Project Task with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/tasks/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Project Task](https://developers.gobridgit.com/reference/projecttasks_remove)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The project ID that the role belongs to |
| `id` | path | `string` | yes | The task ID |
