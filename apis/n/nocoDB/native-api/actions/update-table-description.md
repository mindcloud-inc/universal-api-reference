# Update Table Description with NocoDB

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v3/meta/bases/:baseId/tables/:tableId`
- **Base URL:** `https://app.nocodb.com`
- **Official documentation:** [Update Table Description](https://nocodb.com/apis/v3/meta)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseId` | path | `string` | yes | Base identifier. |
| `tableId` | path | `string` | yes | Table identifier. |
| `description` | body | `string` | yes | New table description. |
