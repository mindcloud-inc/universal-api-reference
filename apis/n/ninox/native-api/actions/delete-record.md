# Delete Record with Ninox

Deletes a record from a Ninox table.

## Endpoint

- **Method:** `DELETE`
- **Path:** `teams/:teamid/databases/:dbid/tables/:tableid/records/:recordid`
- **Base URL:** `https://api.ninox.com/v1`
- **Official documentation:** [Delete Record](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamid` | path | `string` | yes | Workspace ID that owns the database. |
| `dbid` | path | `string` | yes | Database ID that owns the table. |
| `tableid` | path | `string` | yes | Table ID that owns the record. |
| `recordid` | path | `string` | yes | Record ID to delete. |
