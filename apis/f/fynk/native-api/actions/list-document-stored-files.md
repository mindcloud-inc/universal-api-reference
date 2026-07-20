# List Document Stored Files with fynk

Retrieves stored files for a document in fynk.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/:document/file-storage`
- **Base URL:** `https://app.fynk.com/v1/api`
- **Official documentation:** [List Document Stored Files](https://app.fynk.com/v1/docs#/operations/v1.documents.document-file-storage.index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | path | `string` | no | Document UUID. |
