# Get Database Schema with Ninox

Retrieves a database schema from Ninox.

## Endpoint

- **Method:** `GET`
- **Path:** `teams/:teamid/databases/:dbid`
- **Base URL:** `https://api.ninox.com/v1`
- **Official documentation:** [Get Database Schema](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamid` | path | `string` | yes | Workspace ID that owns the database. |
| `dbid` | path | `string` | yes | Database ID to retrieve. |
