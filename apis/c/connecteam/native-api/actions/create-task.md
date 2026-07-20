# Create Task with Connecteam

Create quick task for specified users by their ID, detailing information such as title, due date and description. Attachments for the quick task must first be uploaded via the attachments endpoint.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/v1/taskboards/:taskBoardId/tasks`
- **Base URL:** `https://api.connecteam.com`
- **Official documentation:** [Create Task](https://developer.connecteam.com/reference/create_task_tasks_v1_taskboards__taskBoardId__tasks_post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
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
| `description.content` | body | `string` | yes |
| `description.attachments[]` | body | `array<object>` | no |
| `description.attachments[].fileId` | body | `string` | no |
