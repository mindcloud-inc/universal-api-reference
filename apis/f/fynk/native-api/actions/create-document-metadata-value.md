# Create Document Metadata Value with fynk

Creates a document metadata value in fynk.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/:document/metadata-values`
- **Base URL:** `https://app.fynk.com/v1/api`
- **Official documentation:** [Create Document Metadata Value](https://app.fynk.com/v1/docs#/operations/v1.documents.metadata-values.store)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | path | `string` | no | Document UUID. |
| `metadata_uuid` | body | `string` | no | Metadata UUID to set on the document. |
| `value` | body | `string` | no | Metadata value. |
