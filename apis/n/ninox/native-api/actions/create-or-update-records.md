# Create Or Update Records with Ninox

Creates or updates multiple records in a Ninox table.

## Endpoint

- **Method:** `POST`
- **Path:** `teams/:teamid/databases/:dbid/tables/:tableid/records`
- **Base URL:** `https://api.ninox.com/v1`
- **Official documentation:** [Create Or Update Records](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamid` | path | `string` | yes | Workspace ID that owns the database. |
| `dbid` | path | `string` | yes | Database ID that owns the table. |
| `tableid` | path | `string` | yes | Table ID to create or update records in. |
| `records` | body | `list<object>` | yes | Array of record payloads to create or update. |
