# Rename Table with NocoDB

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v3/meta/bases/:baseId/tables/:tableId`
- **Base URL:** `https://app.nocodb.com`
- **Official documentation:** [Rename Table](https://nocodb.com/apis/v3/meta)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseId` | path | `string` | yes | Base identifier. |
| `tableId` | path | `string` | yes | Table identifier. |
| `title` | body | `string` | yes | New title of the table. |
