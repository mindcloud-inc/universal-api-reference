# Unlink Records with NocoDB

Unlinks records from a NocoDB link field.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v3/data/:baseId/:tableId/links/:linkFieldId/:recordId`
- **Base URL:** `https://app.nocodb.com`
- **Official documentation:** [Unlink Records](https://nocodb.com/apis/v3/data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseId` | path | `string` | yes | Base identifier. |
| `tableId` | path | `string` | yes | Table identifier. |
| `linkFieldId` | path | `string` | yes | Link-to-another-record field identifier. |
| `recordId` | path | `string` | yes | Record identifier. |
| `id` | body | `string` | yes | Adjacent record identifier to unlink. |
