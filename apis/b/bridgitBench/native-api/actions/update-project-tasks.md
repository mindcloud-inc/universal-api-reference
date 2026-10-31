# Update Project Tasks with Bridgit Bench

## Endpoint

- **Method:** `PUT`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/tasks`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Update Project Tasks](https://developers.gobridgit.com/reference/projecttasks_update)

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
| `payload[].id` | body | `string` | yes | — |
| `payload[].name` | body | `string` | no | — |
| `payload[].startDate` | body | `date` | no | — |
| `payload[].endDate` | body | `date` | no | — |
| `payload[].shiftDates` | body | `boolean` | yes | If this property is true and you specify a changed task start or end date in this request, then the task's start and end dates, and the start and end dates for all task roles will be adjusted by the same amount. If this property is set to true, then you must only send EITHER startDate OR endDate - behavior when setting both is to shift with the task start date |
| `payload[].shiftSubsequentTasks` | body | `boolean` | no | Used to shift subsequent tasks when the END DATE of this task is changed. If true, subsequent tasks will be shifted by the same number of days as this task |
