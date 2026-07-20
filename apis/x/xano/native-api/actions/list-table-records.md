# List Table Records with Xano

Finds records in a Xano table.

## Endpoint

- **Method:** `GET`
- **Path:** `/api%3Ameta/workspace/:workspace_id/table/:table_id/content`
- **Base URL:** `https://x8ki-letl-twmt.n7.xano.io`
- **Official documentation:** [List Table Records](https://docs.xano.com/xano-features/metadata-api/tables-and-schema)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `table_id` | path | `number` | yes |
| `workspace_id` | path | `number` | yes |
