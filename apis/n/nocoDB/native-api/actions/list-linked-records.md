# List Linked Records with NocoDB

Retrieves linked records from a NocoDB link field.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/data/:baseId/:tableId/links/:linkFieldId/:recordId`
- **Base URL:** `https://app.nocodb.com`
- **Official documentation:** [List Linked Records](https://nocodb.com/apis/v3/data)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseId` | path | `string` | yes | Base identifier. |
| `tableId` | path | `string` | yes | Table identifier. |
| `linkFieldId` | path | `string` | yes | Link-to-another-record field identifier. |
| `recordId` | path | `string` | yes | Record identifier. |
| `fields` | query | `string` | no | Comma-separated linked-record fields to include. |
| `where` | query | `string` | no | Filter expression in NocoDB where syntax. |
