# Delete Task with Connecteam

Delete quick task under a specified task board

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tasks/v1/taskboards/:taskBoardId/tasks/:taskId`
- **Base URL:** `https://api.connecteam.com`
- **Official documentation:** [Delete Task](https://developer.connecteam.com/reference/delete_task_tasks_v1_taskboards__taskBoardId__tasks__taskId__delete)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `taskId` | path | `string` | yes |
| `taskBoardId` | path | `string` | yes |
