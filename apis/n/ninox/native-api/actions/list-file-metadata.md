# List File Metadata with Ninox

Retrieves metadata for files in a Ninox record.

## Endpoint

- **Method:** `GET`
- **Path:** `teams/:teamId/databases/:dbId/tables/:tableId/records/:recordId/files`
- **Base URL:** `https://api.ninox.com/v1`
- **Official documentation:** [List File Metadata](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | The team ID that owns the target database. |
| `dbId` | path | `string` | yes | The Ninox database ID. |
| `tableId` | path | `string` | yes | The Ninox table ID. |
| `recordId` | path | `string` | yes | The Ninox record ID. |
