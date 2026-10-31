# Create Project Task Role with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/tasks/:id/roles`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Project Task Role](https://developers.gobridgit.com/reference/projecttasks_addrole)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The project ID the task belongs to |
| `id` | path | `string` | yes | The task ID the task belongs to |
| `name` | body | `string` | yes | — |
| `skillSet[]` | body | `array<number>` | yes | — |
| `note` | body | `string` | no | Maximum length: 250. |
| `billable` | body | `boolean` | yes | — |
| `allocatedPercent` | body | `number` | yes | — |
