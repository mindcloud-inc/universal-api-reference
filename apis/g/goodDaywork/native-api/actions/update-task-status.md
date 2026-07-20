# Update Task Status with GoodDay.work

Updates the status of a GoodDay.work task.

## Endpoint

- **Method:** `PUT`
- **Path:** `/task/:taskId/status`
- **Base URL:** `https://api.goodday.work/2.0`
- **Official documentation:** [Update Task Status](https://www.goodday.work/developers/api-v2/tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | GoodDay task ID. |
| `userId` | body | `string` | yes | User on behalf of whom status update is executed. |
| `statusId` | body | `string` | yes | New status ID. |
| `message` | body | `string` | no | Optional status comment. |
