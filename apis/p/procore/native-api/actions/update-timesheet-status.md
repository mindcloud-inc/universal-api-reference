# Update Timesheet Status with Procore

Updates a timesheet approval status in Procore.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rest/v1.0/projects/:project_id/timesheets/update_approval`
- **Base URL:** `https://api.procore.com`
- **Official documentation:** [Update Timesheet Status](https://developers.procore.com/reference/rest/timesheets#update-timesheet-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Unique identifier for the project. |
| `timesheets[]` | body | `array<object>` | yes | Timesheet approval update payload array. |
