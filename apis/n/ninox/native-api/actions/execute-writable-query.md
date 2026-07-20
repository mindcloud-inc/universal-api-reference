# Execute Writable Query with Ninox

Executes a writable database query in Ninox.

## Endpoint

- **Method:** `POST`
- **Path:** `teams/:teamId/databases/:dbId/exec`
- **Base URL:** `https://api.ninox.com/v1`
- **Official documentation:** [Execute Writable Query](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | The team ID that owns the target database. |
| `dbId` | path | `string` | yes | The Ninox database ID. |
| `query` | body | `string` | yes | The writable Ninox query to execute. |
