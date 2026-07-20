# Set Document Fields with Docubee

Sets fields on a document in Docubee.

## Endpoint

- **Method:** `PUT`
- **Path:** `/documents/:documentId/fields`
- **Base URL:** `https://docubee.app/api/v2`
- **Official documentation:** [Set Document Fields](https://docs.docubee.app/#fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | The fields configuration payload. |
| `documentId` | path | `string` | no | The Docubee document ID. |
