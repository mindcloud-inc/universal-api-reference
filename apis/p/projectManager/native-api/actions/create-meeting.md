# Create Meeting with ProjectManager

Creates a new meeting in ProjectManager.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/data/meetings`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Create Meeting](https://developer.projectmanager.com/api-reference/meetings/create-meeting)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | The common name of this Task. |
| `description` | body | `string` | no | This field contains the task's "Note" or "Description", which is a description of the work to be done to complete the task.              Within the ProjectManager application, you can use this field as follows: * When in the Board or List view, click on a task to open the task panel, then edit the "Description" field. |
| `startDate` | body | `string` | no | The date when work on this Task is planned to begin.              This value contains only the date in year-month-day format.  For display, this date will always be shown as this same year-month-day regardless of time zone.  time needs to be in 15-minute increments, valid values are 0, 15, 30, 45 |
| `durationMinutes` | body | `number` | no | The duration (in 15-minute increments) for this Meeting. |
| `assignees[]` | body | `array<string>` | no | Specify a list of resources to assign to this NPT |
| `assignees[]` | body | `array<string>` | no | Specify a list of resources to assign to this NPT |
| `assignees[]` | body | `array<string>` | no | Specify a list of resources to assign to this NPT |
| `priority` | body | `number` | no | The numeric of the Priority for this Meeting |
| `projectId` | body | `string` | no | The unique identifier of the Project for this Meeting |
