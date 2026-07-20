# Update Meeting with ProjectManager

Updates an existing meeting in ProjectManager.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/data/meetings/:meetingId`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Update Meeting](https://developer.projectmanager.com/api-reference/meetings/update-meeting)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meetingId` | path | `string` | yes | the id of the meeting |
| `name` | body | `string` | no | The common name of this Task. |
| `description` | body | `string` | no | This field contains the task's "Note" or "Description", which is a description of the work to be done to complete the task.              Within the ProjectManager application, you can use this field as follows: * When in the Board or List view, click on a task to open the task panel, then edit the "Description" field. |
| `priorityId` | body | `number` | no | Return the priority of a task |
| `plannedStartDate` | body | `string` | no | The date when work on this Task is planned to begin.              This value contains only the date in year-month-day format. For display, this date will always be shown as this same year-month-day regardless of time zone. |
| `durationMinutes` | body | `number` | no | The duration (in 15-minute increments) for this Meeting. |
| `assignees[]` | body | `array<string>` | no | If specified, replaces the list of resources assigned to this meeting. |
| `assignees[]` | body | `array<string>` | no | If specified, replaces the list of resources assigned to this meeting. |
| `assignees[]` | body | `array<string>` | no | If specified, replaces the list of resources assigned to this meeting. |
| `recurring` | body | `boolean` | no | Indicates whether this task participates in a recurring series. true if the task is part of a recurrence (series parent when is, or a child otherwise); false if it is a standalone task. When saved as false during an update, the service layer detaches the task from its series, which clears parent/child relationships including and recurringSettings. |
