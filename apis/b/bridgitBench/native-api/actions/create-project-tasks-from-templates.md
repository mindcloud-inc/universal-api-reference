# Create Project Tasks from Templates with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/tasks/by-templates`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Project Tasks from Templates](https://developers.gobridgit.com/reference/projecttasks_addtasksbytemplates)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The project ID the tasks belongs to |
| `payload[]` | body | `array<object>` | yes | — |
| `payload[].templateId` | body | `string` | yes | — |
| `payload[].startDate` | body | `date` | yes | — |
| `payload[].endDate` | body | `date` | yes | — |
