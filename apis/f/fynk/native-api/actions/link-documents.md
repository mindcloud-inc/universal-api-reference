# Link Documents with fynk

Creates a linked document relationship in fynk.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/:document/linked-documents`
- **Base URL:** `https://app.fynk.com/v1/api`
- **Official documentation:** [Link Documents](https://app.fynk.com/v1/docs#/operations/v1.documents.linked-documents.store)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | path | `string` | no | Document UUID. |
| `other_document_uuid` | body | `string` | no | UUID of the other document to link. |
| `relationship_type` | body | `string` | no | Relationship type between the two documents. |
