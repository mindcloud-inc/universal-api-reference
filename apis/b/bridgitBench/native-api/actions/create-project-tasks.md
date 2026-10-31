# Create Project Tasks with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/tasks`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Project Tasks](https://developers.gobridgit.com/reference/projecttasks_add)

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
| `payload[]` | body | `array<object>` | yes | — |
| `payload[].name` | body | `string` | yes | — |
| `payload[].startDate` | body | `date` | yes | — |
| `payload[].endDate` | body | `date` | yes | — |
