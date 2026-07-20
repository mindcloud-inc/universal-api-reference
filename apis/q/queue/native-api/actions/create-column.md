# Create Column with Queue

Creates a new column for a Queue project.

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:project_id/columns`
- **Base URL:** `https://app.usequeue.com/api/v1`
- **Official documentation:** [Create Column](https://docs.usequeue.com/api-reference/columns/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Required path parameter from projects/:project_id/columns. |
| `title` | query | `string` | no | The title of the column |
| `position` | query | `number` | no | The column's position (0-indexed) within the project |
| `stage` | query | `string` | no | The internal stage type of the column. Can be 'in_queue', 'in_progress', or 'done' |
| `finished` | query | `boolean` | no | Whether tasks in this column are marked as finished |
| `start_timer` | query | `boolean` | no | Whether tasks in this column should start the timer automatically |
