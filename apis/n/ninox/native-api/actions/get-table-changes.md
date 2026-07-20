# Get Table Changes with Ninox

Retrieves table changes from Ninox by sequence number.

## Endpoint

- **Method:** `GET`
- **Path:** `teams/:teamId/databases/:dbId/tables/:tableId/changes`
- **Base URL:** `https://api.ninox.com/v1`
- **Official documentation:** [Get Table Changes](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | The team ID that owns the target database. |
| `dbId` | path | `string` | yes | The Ninox database ID. |
| `tableId` | path | `string` | yes | The Ninox table ID. |
| `sinceSq` | query | `number` | yes | Return changes since this sequence number. |
