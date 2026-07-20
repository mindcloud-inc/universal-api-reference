# Delete Records with Ninox

Deletes multiple records from a Ninox table.

## Endpoint

- **Method:** `DELETE`
- **Path:** `teams/:teamid/databases/:dbid/tables/:tableid/records`
- **Base URL:** `https://api.ninox.com/v1`
- **Official documentation:** [Delete Records](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamid` | path | `string` | yes | Workspace ID that owns the database. |
| `dbid` | path | `string` | yes | Database ID that owns the table. |
| `tableid` | path | `string` | yes | Table ID to delete records from. |
| `record ids` | body | `list<number>` | yes | Array of record IDs to delete. |
