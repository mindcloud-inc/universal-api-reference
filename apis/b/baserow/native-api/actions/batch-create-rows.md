# Batch Create Rows with Baserow

Creates multiple rows in a Baserow table.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/database/rows/table/:table_id/batch/`
- **Base URL:** `https://api.baserow.io`
- **Official documentation:** [Batch Create Rows](https://api.baserow.io/api/redoc/#operation/batch_create_database_table_rows)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `number` | yes | The Baserow table where rows will be created. |
| `user_field_names` | query | `boolean` | no | Use user-facing field names in the request and response. |
| `before` | query | `number` | no | Create the new rows before the given row ID. |
| `include_metadata` | query | `boolean` | no | Include update metadata in the response. |
| `send_webhook_events` | query | `boolean` | no | Whether Baserow should emit webhook events for the mutation. |
| `view` | query | `number` | no | Optional view context for permissions and default values. |
