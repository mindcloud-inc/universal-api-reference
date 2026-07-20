# Create Row with Baserow

Creates a new row in Baserow.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/database/rows/table/:table_id/`
- **Base URL:** `https://api.baserow.io`
- **Official documentation:** [Create Row](https://api.baserow.io/api/redoc/#operation/create_database_table_row)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `number` | yes | The Baserow table where the row will be created. |
| `user_field_names` | query | `boolean` | no | Use user-facing field names in the request and response. |
| `before` | query | `number` | no | Create the new row before the given row ID. |
| `send_webhook_events` | query | `boolean` | no | Whether Baserow should emit webhook events for the mutation. |
| `view` | query | `number` | no | Optional view context for permissions and default values. |
