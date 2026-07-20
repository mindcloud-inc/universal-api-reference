# Delete Table Records with NocoDB

Deletes records from a NocoDB table.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v3/data/:baseId/:tableId/records`
- **Base URL:** `https://app.nocodb.com`
- **Official documentation:** [Delete Table Records](https://nocodb.com/apis/v3/data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseId` | path | `string` | yes | Base identifier. |
| `tableId` | path | `string` | yes | Table identifier. |
| `id` | body | `string` | yes | Record identifier. |
