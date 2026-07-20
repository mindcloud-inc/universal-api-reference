# Update Task with Connecteam

Update a quick task under a specified task board. Any new attachments will replace the existing ones.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/v1/taskboards/:taskBoardId/tasks/:taskId`
- **Base URL:** `https://api.connecteam.com`
- **Official documentation:** [Update Task](https://developer.connecteam.com/reference/update_task_tasks_v1_taskboards__taskBoardId__tasks__taskId__put)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `taskId` | path | `string` | yes |
| `taskBoardId` | path | `string` | yes |
| `userIds[]` | body | `array<number>` | yes |
| `status` | body | `string` | yes |
| `title` | body | `string` | yes |
| `startTime` | body | `number` | no |
| `dueDate` | body | `number` | no |
| `labelIds[]` | body | `array<string>` | no |
| `type` | body | `string` | no |
| `isArchived` | body | `boolean` | no |
| `subTasks[]` | body | `array<object>` | no |
| `subTasks[].title` | body | `string` | yes |
| `subTasks[].isCompleted` | body | `boolean` | no |
| `description` | body | `object` | no |
| `description.content` | body | `string` | no |
| `description.attachments[]` | body | `array<object>` | no |
| `description.attachments[].fileId` | body | `string` | no |
