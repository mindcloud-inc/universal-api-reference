# Batch Delete Rows with Baserow

Deletes multiple rows from a Baserow table.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/database/rows/table/:table_id/batch-delete/`
- **Base URL:** `https://api.baserow.io`
- **Official documentation:** [Batch Delete Rows](https://api.baserow.io/api/redoc/#operation/batch_delete_database_table_rows)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `number` | yes | The Baserow table containing the rows. |
| `items[]` | body | `array<number>` | yes | An array of row IDs to delete. |
| `send_webhook_events` | query | `boolean` | no | Whether Baserow should emit webhook events for the mutation. |
| `view` | query | `number` | no | Optional view context for permissions and default values. |
