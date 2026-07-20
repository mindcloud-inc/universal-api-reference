# Delete Table with Xano

Deletes an existing table from Xano.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api%3Ameta/workspace/:workspace_id/table/:table_id`
- **Base URL:** `https://x8ki-letl-twmt.n7.xano.io`
- **Official documentation:** [Delete Table](https://docs.xano.com/xano-features/metadata-api/tables-and-schema)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `table_id` | path | `number` | yes |
| `workspace_id` | path | `number` | yes |
