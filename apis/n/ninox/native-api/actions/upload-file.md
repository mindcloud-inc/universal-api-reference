# Upload File with Ninox

Uploads a file to a Ninox record.

## Endpoint

- **Method:** `POST`
- **Path:** `teams/:teamId/databases/:dbId/tables/:tableId/records/:recordId/files`
- **Base URL:** `https://api.ninox.com/v1`
- **Official documentation:** [Upload File](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | The team ID that owns the target database. |
| `dbId` | path | `string` | yes | The Ninox database ID. |
| `tableId` | path | `string` | yes | The Ninox table ID. |
| `recordId` | path | `string` | yes | The Ninox record ID. |
| `file` | body | `file` | yes | The file to upload as multipart/form-data. |
