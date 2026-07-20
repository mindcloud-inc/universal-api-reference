# Delete Table Record with Xano

Deletes an existing record from a Xano table.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api%3Ameta/workspace/:workspace_id/table/:table_id/content/:content_id`
- **Base URL:** `https://x8ki-letl-twmt.n7.xano.io`
- **Official documentation:** [Delete Table Record](https://docs.xano.com/xano-features/metadata-api/tables-and-schema)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `content_id` | path | `number` | yes |
| `table_id` | path | `number` | yes |
| `workspace_id` | path | `number` | yes |
