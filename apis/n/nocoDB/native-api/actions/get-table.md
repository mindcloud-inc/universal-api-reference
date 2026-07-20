# Get Table with NocoDB

Retrieves table schema details from NocoDB.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/meta/bases/:baseId/tables/:tableId`
- **Base URL:** `https://app.nocodb.com`
- **Official documentation:** [Get Table](https://nocodb.com/apis/v3/meta)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseId` | path | `string` | yes | Base identifier. |
| `tableId` | path | `string` | yes | Table identifier. |
