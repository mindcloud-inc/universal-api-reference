# Create Task with GanttPRO

Creates a new task in GanttPRO.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://api.ganttpro.com/v1.0`
- **Official documentation:** [Create Task](https://developer.ganttpro.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | body | `number` | yes | Project identifier for the new task. |
| `name` | body | `string` | yes | Task name. |
| `parent` | body | `number` | no | Optional parent task identifier. |
| `startDate` | body | `date` | no | Task start date. |
| `endDate` | body | `date` | no | Task end date. |
| `description` | body | `string` | no | Task description. |
