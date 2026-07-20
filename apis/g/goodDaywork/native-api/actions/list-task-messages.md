# List Task Messages with GoodDay.work

Finds messages on a GoodDay.work task.

## Endpoint

- **Method:** `GET`
- **Path:** `/task/:taskId/messages`
- **Base URL:** `https://api.goodday.work/2.0`
- **Official documentation:** [List Task Messages](https://www.goodday.work/developers/api-v2/tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | GoodDay task ID. |
