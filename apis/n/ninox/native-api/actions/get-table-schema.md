# Get Table Schema with Ninox

Retrieves a table schema from Ninox.

## Endpoint

- **Method:** `GET`
- **Path:** `teams/:teamid/databases/:dbid/tables/:tableid`
- **Base URL:** `https://api.ninox.com/v1`
- **Official documentation:** [Get Table Schema](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamid` | path | `string` | yes | Workspace ID that owns the database. |
| `dbid` | path | `string` | yes | Database ID that owns the table. |
| `tableid` | path | `string` | yes | Table ID to retrieve. |
