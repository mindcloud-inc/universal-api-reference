# List Tasks with Connecteam

Retrieves a list of tasks under a specified task board

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/v1/taskboards/:taskBoardId/tasks`
- **Base URL:** `https://api.connecteam.com`
- **Official documentation:** [List Tasks](https://developer.connecteam.com/reference/get_tasks_tasks_v1_taskboards__taskBoardId__tasks_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskBoardId` | path | `string` | yes | — |
| `taskIds` | query | `array<string>` | no | Send multiple values as a array. |
| `labelIds` | query | `array<string>` | no | Send multiple values as a array. |
| `userIds` | query | `array<number>` | no | Send multiple values as a array. |
| `status` | query | `string` | no | — |
| `limit` | query | `number` | no | — |
| `offset` | query | `number` | no | — |
