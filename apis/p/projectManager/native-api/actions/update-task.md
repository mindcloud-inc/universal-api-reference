# Update Task with ProjectManager

Updates an existing task in ProjectManager.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/data/tasks/:taskId`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Update Task](https://developer.projectmanager.com/api-reference/task/update-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The unique identifier of the Task to update |
| `name` | body | `string` | no | The common name of this Task. |
| `description` | body | `string` | no | A description of the work to be performed in this Task. |
| `percentComplete` | body | `number` | no | The numerical percentage, from 0-100, representing the percentage completion for this Task.  Any numbers below zero or above 100 will be clamped to the minimum or maximum value.              This value can be edited manually in the Gantt chart view of the application, or can be selected on the Task Detail page within the Kanban board. |
| `statusId` | body | `string` | no | The TaskStatus assigned to this Task. |
| `priorityId` | body | `number` | no | The unique identifier of the TaskPriority |
| `plannedStartDate` | body | `string` | no | The date when work on this Task is planned to begin.              This value contains only the date in year-month-day format.  For display, this date will always be shown as this same year-month-day regardless of time zone. For reporting purposes, this date is calculated against the official time zone of the Workspace.              For example: A Task has a planned completion date of July 5, 2023 in a Workspace that has a time zone of US Pacific Time (GMT-7 or GMT-8, depending on daylight savings time).  This project is considered overdue on 12:01 AM July 6th 2023 in US Pacific time. |
| `plannedFinishDate` | body | `string` | no | The date when work on this Task is expected to complete.              This value contains only the date in year-month-day format.  For display, this date will always be shown as this same year-month-day regardless of time zone. For reporting purposes, this date is calculated against the official time zone of the Workspace.              For example: A Task has a planned completion date of July 5, 2023 in a Workspace that has a time zone of US Pacific Time (GMT-7 or GMT-8, depending on daylight savings time).  This project is considered overdue on 12:01 AM July 6th 2023 in US Pacific time. |
| `plannedDuration` | body | `number` | no | The planned duration (in minutes) for this Task.  Cannot be negative. |
| `plannedEffort` | body | `number` | no | The planned effort (in minutes) for this Task.  Cannot be negative. |
| `plannedCost` | body | `number` | no | The planned cost for this Task.  Cannot be negative. |
| `actualStartDate` | body | `string` | no | If set, this is the actual date when work began on the Task.              This value contains only the date in year-month-day format.  For display, this date will always be shown as this same year-month-day regardless of time zone. For reporting purposes, this date is calculated against the official time zone of the Workspace.              For example: A Task has a planned completion date of July 5, 2023 in a Workspace that has a time zone of US Pacific Time (GMT-7 or GMT-8, depending on daylight savings time).  This project is considered overdue on 12:01 AM July 6th 2023 in US Pacific time. |
| `actualFinishDate` | body | `string` | no | If set, this is the actual date when work was completed on the Task.              This value contains only the date in year-month-day format.  For display, this date will always be shown as this same year-month-day regardless of time zone. For reporting purposes, this date is calculated against the official time zone of the Workspace.              For example: A Task has a planned completion date of July 5, 2023 in a Workspace that has a time zone of US Pacific Time (GMT-7 or GMT-8, depending on daylight savings time).  This project is considered overdue on 12:01 AM July 6th 2023 in US Pacific time. |
| `actualDuration` | body | `number` | no | The actual duration (in minutes) for this Task.  Cannot be negative. |
| `actualCost` | body | `number` | no | If set, this represents the actual tracked cost for this Task. |
| `theme` | body | `string` | no | Color theme definition for this task.              eg. Blue, Brown, DarkBlue, DarkGrey, Gold, Green, Grey, LightBrown, LightGreen, LightGrey, LightPurple, LightYellow, Magenta, Mauve, Navy, Orange, Purple, Red. |
| `isLocked` | body | `boolean` | no | Unlocked tasks can be adjusted by changes to their dependencies, resource leveling, or other factors.              All tasks are unlocked by default.              If a task is set to `IsLocked` = `true`, the dates and assigned resources are locked for this task and will not be automatically changed by any process. |
| `isMilestone` | body | `boolean` | no | True if this task is a milestone.  Milestones represent a specific point in time for the project.  When a milestone is locked, it represents a fixed time within the project that can be used to relate to other tasks. |
