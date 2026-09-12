# List Worker Time Blocks with Workday

List worker time blocks from Workday Time Tracking so you can review timesheet-style entries by worker, date range, status, project, or task.

## Endpoint

- **Method:** `GET`
- **Path:** `/workerTimeBlocks`
- **Base URL:** `{restAPIBaseURL}/`
- **Official documentation:** [List Worker Time Blocks](https://community.workday.com/sites/default/files/file-hosting/restapi/index.html#timeTracking/v5/get-/workerTimeBlocks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `worker` | query | `string<string>` | no | The Workday ID of the worker for the time block filter. |
| `fromDate` | query | `date` | no | Start date of the time block date range filter. |
| `toDate` | query | `date` | no | End date of the time block date range filter. |
| `status` | query | `string<string>` | no | The Workday ID of the approval status for the time block filter. |
| `phase` | query | `string<string>` | no | The Workday ID of the project plan phase filter. |
| `project` | query | `string<string>` | no | The Workday ID of the project filter. |
| `projectPlanTask` | query | `string<string>` | no | The Workday ID of the project plan task filter. |
