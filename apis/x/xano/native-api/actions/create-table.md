# Create Table with Xano

Creates a new table in a Xano workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/api%3Ameta/workspace/:workspace_id/table`
- **Base URL:** `https://x8ki-letl-twmt.n7.xano.io`
- **Official documentation:** [Create Table](https://docs.xano.com/xano-features/metadata-api/tables-and-schema)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `workspace_id` | path | `number` | yes |
