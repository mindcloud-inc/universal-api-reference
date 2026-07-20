# Update Task Status in Batch with Wodely

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/tasks/status`
- **Base URL:** `https://api.wodely.com`
- **Official documentation:** [Update Task Status in Batch](https://app.wodely.com/doc/api-documentation.html#update-task-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `updates[].taskGuid` | body | `string` | yes | Task Id. |
| `updates[].statusId` | body | `number` | yes | 10:Unassigned 15:Assigning 20:Assigned 25:Processed 28:Loaded 30:Transit 40:Arrived 45:Awaiting Collection 50:Completed 51:Failed 52:Returned 90:Cancelled. |
