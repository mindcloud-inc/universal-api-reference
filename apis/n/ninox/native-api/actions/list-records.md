# List Records with Ninox

Retrieves records from a Ninox table.

## Endpoint

- **Method:** `GET`
- **Path:** `teams/:teamid/databases/:dbid/tables/:tableid/records`
- **Base URL:** `https://api.ninox.com/v1`
- **Official documentation:** [List Records](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamid` | path | `string` | yes | Workspace ID that owns the database. |
| `dbid` | path | `string` | yes | Database ID that owns the table. |
| `tableid` | path | `string` | yes | Table ID whose records to list. |
| `choiceStyle` | query | `string` | no | Optional choice formatting style for returned fields. |
