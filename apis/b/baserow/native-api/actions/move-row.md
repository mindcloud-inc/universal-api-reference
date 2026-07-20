# Move Row with Baserow

Moves an existing row in a Baserow table.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/database/rows/table/:table_id/:row_id/move/`
- **Base URL:** `https://api.baserow.io`
- **Official documentation:** [Move Row](https://api.baserow.io/api/redoc/#operation/move_database_table_row)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `number` | yes | The Baserow table containing the row. |
| `row_id` | path | `number` | yes | The row to move. |
| `before_id` | query | `number` | no | Move the row before this row ID. Leave empty to move it to the end. |
| `send_webhook_events` | query | `boolean` | no | Whether Baserow should emit webhook events for the mutation. |
| `user_field_names` | query | `boolean` | no | Use user-facing field names in the response. |
