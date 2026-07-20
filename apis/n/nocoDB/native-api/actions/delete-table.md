# Delete Table with NocoDB

Deletes an existing table from NocoDB.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v3/meta/bases/:baseId/tables/:tableId`
- **Base URL:** `https://app.nocodb.com`
- **Official documentation:** [Delete Table](https://nocodb.com/apis/v3/meta)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseId` | path | `string` | yes | Base identifier. |
| `tableId` | path | `string` | yes | Table identifier. |
