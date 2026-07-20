# Create Project Timesheet with Queue

Creates a new timesheet for a Queue project.

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:project_id/timesheets`
- **Base URL:** `https://app.usequeue.com/api/v1`
- **Official documentation:** [Create Project Timesheet](https://docs.usequeue.com/api-reference/timesheets/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | — |
| `task_id` | query | `string` | yes | — |
| `notes` | query | `string` | no | — |
| `duration` | query | `number` | yes | Duration of the timesheet in milliseconds |
