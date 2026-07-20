# Update Task with TickTick

Updates an existing task in TickTick.

## Endpoint

- **Method:** `POST`
- **Path:** `/open/v1/task/:taskId`
- **Base URL:** `https://api.ticktick.com`
- **Official documentation:** [Update Task](https://developer.ticktick.com/docs/index.html#/openapi?id=update-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | Task identifier |
| `id` | body | `string` | yes | Task ID in request body |
| `projectId` | body | `list<string>` | yes | Project identifier |
| `title` | body | `string` | no | Task title |
| `content` | body | `string` | no | Task content |
| `desc` | body | `string` | no | Task description |
| `isAllDay` | body | `boolean` | no | Whether task is all day |
| `startDate` | body | `string` | no | Task start date time |
| `dueDate` | body | `string` | no | Task due date time |
| `timeZone` | body | `string` | no | Task time zone |
| `priority` | body | `number` | no | Task priority |
| `reminders[]` | body | `array<string>` | no | List of reminder triggers |
| `repeatFlag` | body | `string` | no | Recurring rules of task |
| `sortOrder` | body | `number` | no | Task order |
| `items[]` | body | `array<object>` | no | List of subtasks |
| `items[].title` | body | `string` | no | Subtask title |
| `items[].startDate` | body | `date` | no | Subtask start date/time |
| `items[].isAllDay` | body | `boolean` | no | Whether subtask is all day |
| `items[].sortOrder` | body | `number` | no | Subtask order |
| `items[].timeZone` | body | `string` | no | Subtask time zone |
| `items[].status` | body | `number` | no | Subtask completion status |
| `items[].completedTime` | body | `date` | no | Subtask completed time |
