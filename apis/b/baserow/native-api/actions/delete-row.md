# Delete Row with Baserow

Deletes an existing row from Baserow.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/database/rows/table/:table_id/:row_id/`
- **Base URL:** `https://api.baserow.io`
- **Official documentation:** [Delete Row](https://api.baserow.io/api/redoc/#operation/delete_database_table_row)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `number` | yes | The Baserow table containing the row. |
| `row_id` | path | `number` | yes | The row to delete. |
| `send_webhook_events` | query | `boolean` | no | Whether Baserow should emit webhook events for the mutation. |
| `view` | query | `number` | no | Optional view context for permissions and default values. |
