# List User Action Required Tasks with GoodDay.work

Finds tasks requiring action from a GoodDay.work user.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/:userId/action-required-tasks`
- **Base URL:** `https://api.goodday.work/2.0`
- **Official documentation:** [List User Action Required Tasks](https://www.goodday.work/developers/api-v2/tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | GoodDay user ID. |
