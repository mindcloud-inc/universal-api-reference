# Update Timesheet with Queue

Updates an existing timesheet in Queue.

## Endpoint

- **Method:** `PATCH`
- **Path:** `timesheets/:timesheet_id`
- **Base URL:** `https://app.usequeue.com/api/v1`
- **Official documentation:** [Update Timesheet](https://docs.usequeue.com/api-reference/timesheets/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `timesheet_id` | path | `string` | yes | — |
| `task_id` | query | `string` | yes | — |
| `notes` | query | `string` | no | — |
| `duration` | query | `number` | yes | Duration of the timesheet in milliseconds |
