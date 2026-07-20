# Comment On Task with GoodDay.work

Creates a comment on a GoodDay.work task.

## Endpoint

- **Method:** `POST`
- **Path:** `/task/:taskId/comment`
- **Base URL:** `https://api.goodday.work/2.0`
- **Official documentation:** [Comment On Task](https://www.goodday.work/developers/api-v2/tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | GoodDay task ID. |
| `userId` | body | `string` | yes | User on behalf of whom comment is created. |
| `message` | body | `string` | no | Comment message. |
