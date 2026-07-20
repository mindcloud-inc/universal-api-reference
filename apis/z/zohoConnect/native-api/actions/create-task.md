# Create Task with Zoho Connect

Creates a new task in Zoho Connect.

## Endpoint

- **Method:** `POST`
- **Path:** `/pulse/api/addTask`
- **Base URL:** `https://connect.zoho.com`
- **Official documentation:** [Create Task](https://www.zoho.com/connect/api/create-task.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `boardId` | query | `string` | no | ID of the board to add the task to. |
| `checkList` | query | `string` | no | Checklist items for the task. |
| `dayOfMonth` | query | `number` | no | Monthly repeat day. |
| `dayOfWeek` | query | `string` | no | Weekly repeat days. Send multiple values as a string separated by `,`. |
| `desc` | query | `string` | no | Task description. |
| `edate` | query | `number` | no | Due date day. |
| `emonth` | query | `number` | no | Due date month. |
| `eyear` | query | `number` | no | Due date year. |
| `fileIds` | query | `string` | no | Comma-separated file IDs to attach to the task. Send multiple values as a string separated by `,`. |
| `howOftenRepetition` | query | `number` | no | How often the task repeats. |
| `isSelfReminder` | query | `boolean` | no | Whether the task should include a reminder. |
| `monthOfYear` | query | `number` | no | Month of the year for yearly recurring tasks. |
| `position` | query | `number` | yes | Board task position. |
| `priority` | query | `string` | yes | Priority level: None, Low, Medium, or High. |
| `remDay` | query | `number` | no | Task reminder day. |
| `remHour` | query | `number` | no | Task reminder hour in 24-hour format. |
| `remMin` | query | `number` | no | Task reminder minute. |
| `remMonth` | query | `number` | no | Task reminder month. |
| `remYear` | query | `number` | no | Task reminder year. |
| `repeatEndDate` | query | `number` | no | Day of month when task recurrence should end. |
| `repeatEndMonth` | query | `number` | no | Month when task recurrence should end. |
| `repeatEndYear` | query | `number` | no | Year when task recurrence should end. |
| `scopeID` | query | `string` | yes | ID of the network where the task is created. |
| `sectionId` | query | `string` | yes | Board section to place the task in. |
| `streamId` | query | `string` | no | Optional stream ID to link a task to a post. |
| `tagColors` | query | `string` | no | Colors for task tags. Send multiple values as a string separated by `,`. |
| `tagNames` | query | `string` | no | Hashtag names associated with the task. Send multiple values as a string separated by `,`. |
| `title` | query | `string` | yes | Task title. |
| `userIds` | query | `string` | no | Comma-separated user IDs to assign to the task. Send multiple values as a string separated by `,`. |
