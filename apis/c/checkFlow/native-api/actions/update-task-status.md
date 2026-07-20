# Update Task Status with CheckFlow

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/task/status`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [Update Task Status](https://docs.checkflow.io/docs/api/tasks#update-task-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskID` | body | `number` | yes | The ID of the task to update. |
| `status` | body | `string` | yes | The new status. Values: Complete, Incomplete, NotApplicable. |
| `modifiedByUserID` | body | `number` | yes | The ID of the user updating the task status. |
