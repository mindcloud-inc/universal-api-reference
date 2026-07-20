# Batch Update Rows with Baserow

Updates multiple rows in a Baserow table.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/database/rows/table/:table_id/batch/`
- **Base URL:** `https://api.baserow.io`
- **Official documentation:** [Batch Update Rows](https://api.baserow.io/api/redoc/#operation/batch_update_database_table_rows)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `number` | yes | The Baserow table containing the rows. |
| `user_field_names` | query | `boolean` | no | Use user-facing field names in the request and response. |
| `include_metadata` | query | `boolean` | no | Include update metadata in the response. |
| `send_webhook_events` | query | `boolean` | no | Whether Baserow should emit webhook events for the mutation. |
| `view` | query | `number` | no | Optional view context for permissions and default values. |
