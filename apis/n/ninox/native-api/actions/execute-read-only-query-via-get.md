# Execute Read-Only Query Via GET with Ninox

Executes a read-only database query in Ninox.

## Endpoint

- **Method:** `GET`
- **Path:** `teams/:teamId/databases/:dbId/query`
- **Base URL:** `https://api.ninox.com/v1`
- **Official documentation:** [Execute Read-Only Query Via GET](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | The team ID that owns the target database. |
| `dbId` | path | `string` | yes | The Ninox database ID. |
| `query` | query | `string` | yes | The read-only Ninox query to execute. |
