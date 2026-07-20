# Update Column with Queue

Updates an existing column in Queue.

## Endpoint

- **Method:** `PATCH`
- **Path:** `columns/:column_id`
- **Base URL:** `https://app.usequeue.com/api/v1`
- **Official documentation:** [Update Column](https://docs.usequeue.com/api-reference/columns/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `column_id` | path | `string` | yes | Required path parameter from columns/:column_id. |
| `title` | query | `string` | no | The title of the column |
| `position` | query | `number` | no | The column's position (0-indexed) within the project |
| `stage` | query | `string` | no | The internal stage type of the column. Can be 'in_queue', 'in_progress', or 'done' |
| `finished` | query | `boolean` | no | Whether tasks in this column are marked as finished |
| `start_timer` | query | `boolean` | no | Whether tasks in this column should start the timer automatically |
