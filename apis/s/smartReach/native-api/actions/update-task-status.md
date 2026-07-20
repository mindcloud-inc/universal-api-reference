# Update Task Status with SmartReach

Updates task status in SmartReach.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/:task_id/status`
- **Base URL:** `https://api.smartreach.io/api/v3`
- **Official documentation:** [Update Task Status](https://help.smartreach.io/reference/changetaskstatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | Task UUID |
| `due_at` | body | `number` | no | The date-time with respective time-zone of schedule start should be converted to Epoch milliseconds and passed. |
| `status_type` | body | `string` | no | — |
| `snoozed_till` | body | `number` | no | DateTime until when the task is snoozed.The date-time with respective time-zone of schedule start should be converted to Epoch milliseconds and passed. |
