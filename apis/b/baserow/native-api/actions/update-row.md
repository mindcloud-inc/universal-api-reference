# Update Row with Baserow

Updates an existing row in Baserow.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/database/rows/table/:table_id/:row_id/`
- **Base URL:** `https://api.baserow.io`
- **Official documentation:** [Update Row](https://api.baserow.io/api/redoc/#operation/update_database_table_row)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `number` | yes | The Baserow table containing the row. |
| `row_id` | path | `number` | yes | The row to update. |
| `user_field_names` | query | `boolean` | no | Use user-facing field names in the request and response. |
| `send_webhook_events` | query | `boolean` | no | Whether Baserow should emit webhook events for the mutation. |
| `view` | query | `number` | no | Optional view context for permissions and default values. |
