# Update Project Task Role with Bridgit Bench

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/tasks/:taskId/roles/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Update Project Task Role](https://developers.gobridgit.com/reference/projecttasks_updaterole)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The project ID |
| `taskId` | path | `string` | yes | The task ID |
| `id` | path | `number` | yes | The role ID the task role belongs to |
| `name` | body | `string` | yes | — |
| `skillSet[]` | body | `array<number>` | yes | — |
| `note` | body | `string` | no | Maximum length: 250. |
| `billable` | body | `boolean` | no | — |
| `allocatedPercent` | body | `number` | no | — |
