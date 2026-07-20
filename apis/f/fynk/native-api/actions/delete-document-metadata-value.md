# Delete Document Metadata Value with fynk

Deletes a document metadata value from fynk.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/documents/:document/metadata-values/:metadataValue`
- **Base URL:** `https://app.fynk.com/v1/api`
- **Official documentation:** [Delete Document Metadata Value](https://app.fynk.com/v1/docs#/operations/v1.documents.metadata-values.destroy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | path | `string` | no | Document UUID. |
| `metadataValue` | path | `string` | no | Metadata value UUID. |
