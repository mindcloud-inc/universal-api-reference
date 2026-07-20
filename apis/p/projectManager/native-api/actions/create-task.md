# Create Task with ProjectManager

Creates a new task in ProjectManager.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/data/projects/:projectId/tasks`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Create Task](https://developer.projectmanager.com/api-reference/task/create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The unique identifier of the Project that will contain this Task |
| `name` | body | `string` | yes | The common name of this Task. |
| `description` | body | `string` | no | A description of the work to be performed in this Task. |
| `percentComplete` | body | `number` | no | The numerical percentage, from 0-100, representing the percentage completion for this Task.  Any numbers below zero or above 100 will be clamped to the minimum or maximum value.              This value can be edited manually in the Gantt chart view of the application, or can be selected on the Task Detail page within the Kanban board. |
| `statusId` | body | `string` | no | The unique identifier of the TaskStatus for this Task |
| `priorityId` | body | `number` | no | A numerical value representing the Priority of this Task |
| `assignees[]` | body | `array<string>` | no | A list of unique identifiers of TaskAssignees to be assigned to this Task |
| `assignees[]` | body | `array<string>` | no | A list of unique identifiers of TaskAssignees to be assigned to this Task |
| `assignees[]` | body | `array<string>` | no | A list of unique identifiers of TaskAssignees to be assigned to this Task |
| `plannedStartDate` | body | `string` | no | The date when work on this Task is planned to begin. |
| `plannedFinishDate` | body | `string` | no | The date when work on this Task is expected to complete. |
| `plannedDuration` | body | `number` | no | The planned duration (in minutes) for this Task.  Cannot be negative. |
| `plannedEffort` | body | `number` | no | The planned effort (in minutes) for this Task.  Cannot be negative. |
| `plannedCost` | body | `number` | no | The planned cost for this Task.  Cannot be negative. |
| `actualStartDate` | body | `string` | no | The date when work on this Task actually started, if known. |
| `actualCost` | body | `number` | no | The actual cost of this Task to date, if known. |
| `theme` | body | `string` | no | Color theme definition for this task.              eg. Blue, Brown, DarkBlue, DarkGrey, Gold, Green, Grey, LightBrown, LightGreen, LightGrey, LightPurple, LightYellow, Magenta, Mauve, Navy, Orange, Purple, Red. |
| `isLocked` | body | `boolean` | no | Unlocked tasks can be adjusted by changes to their dependencies, resource leveling, or other factors.              All tasks are unlocked by default.              If a task is set to `IsLocked` = `true`, the dates and assigned resources are locked for this task and will not be automatically changed by any process. |
| `isMilestone` | body | `boolean` | no | True if this task is a milestone.  Milestones represent a specific point in time for the project.  When a milestone is locked, it represents a fixed time within the project that can be used to relate to other tasks. |
| `parentId` | body | `string` | no | Gets or sets the unique identifier of the parent task. If set, this task will be a child of the specified parent task, supporting task hierarchies and sub-tasks. |
| `index` | body | `number` | no | Gets or sets the position of the task within the list of project tasks. Used to determine the order of tasks in the project with the first task being 1. |
