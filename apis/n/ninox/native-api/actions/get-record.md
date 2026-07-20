# Get Record with Ninox

Retrieves a record from a Ninox table.

## Endpoint

- **Method:** `GET`
- **Path:** `teams/:teamid/databases/:dbid/tables/:tableid/records/:recordid`
- **Base URL:** `https://api.ninox.com/v1`
- **Official documentation:** [Get Record](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamid` | path | `string` | yes | Workspace ID that owns the database. |
| `dbid` | path | `string` | yes | Database ID that owns the table. |
| `tableid` | path | `string` | yes | Table ID that owns the record. |
| `recordid` | path | `string` | yes | Record ID to retrieve. |
| `choiceStyle` | query | `string` | no | Optional choice formatting style for returned fields. |
