# Get Column Tasks with Queue

Retrieves tasks for a Queue column.

## Endpoint

- **Method:** `GET`
- **Path:** `columns/:column_id/tasks`
- **Base URL:** `https://app.usequeue.com/api/v1`
- **Official documentation:** [Get Column Tasks](https://docs.usequeue.com/api-reference/tasks/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `column_id` | path | `string` | yes | Required path parameter from columns/:column_id/tasks. |
| `project_id` | query | `string` | yes | — |
