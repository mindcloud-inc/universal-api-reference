# Search Table Records with Xano

Finds records in a Xano table by search filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/api%3Ameta/workspace/:workspace_id/table/:table_id/content/search`
- **Base URL:** `https://x8ki-letl-twmt.n7.xano.io`
- **Official documentation:** [Search Table Records](https://docs.xano.com/xano-features/metadata-api/tables-and-schema)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `table_id` | path | `number` | yes |
| `workspace_id` | path | `number` | yes |
