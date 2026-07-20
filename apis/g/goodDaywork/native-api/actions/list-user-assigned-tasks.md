# List User Assigned Tasks with GoodDay.work

Finds tasks assigned to a GoodDay.work user.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/:userId/assigned-tasks`
- **Base URL:** `https://api.goodday.work/2.0`
- **Official documentation:** [List User Assigned Tasks](https://www.goodday.work/developers/api-v2/tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | GoodDay user ID. |
