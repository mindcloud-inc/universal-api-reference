# Update Task Control Value with CheckFlow

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/task/update-task-content`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [Update Task Control Value](https://docs.checkflow.io/docs/api/tasks#update-task-control-value)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskContentID` | body | `number` | yes | The ID of the task content record. |
| `contentID` | body | `number` | yes | The ID of the content control. |
| `key` | body | `string` | yes | The key of the content control. |
| `contentType` | body | `string` | yes | The type of control being updated. |
| `name` | body | `string` | yes | The label or name of the control. |
| `value` | body | `string` | yes | The value to set. Format depends on the content type. |
