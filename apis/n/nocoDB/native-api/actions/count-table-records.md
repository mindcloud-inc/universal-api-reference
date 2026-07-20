# Count Table Records with NocoDB

Counts records in a NocoDB table.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/data/:baseId/:tableId/count`
- **Base URL:** `https://app.nocodb.com`
- **Official documentation:** [Count Table Records](https://nocodb.com/apis/v3/data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseId` | path | `string` | yes | Base identifier. |
| `tableId` | path | `string` | yes | Table identifier. |
| `where` | query | `string` | no | Filter expression in NocoDB where syntax. |
