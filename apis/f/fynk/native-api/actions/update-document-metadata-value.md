# Update Document Metadata Value with fynk

Updates a document metadata value in fynk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/documents/:document/metadata-values/:metadataValue`
- **Base URL:** `https://app.fynk.com/v1/api`
- **Official documentation:** [Update Document Metadata Value](https://app.fynk.com/v1/docs#/operations/v1.documents.metadata-values.update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | path | `string` | no | Document UUID. |
| `metadataValue` | path | `string` | no | Metadata value UUID. |
| `value` | body | `string` | no | Updated metadata value. |
