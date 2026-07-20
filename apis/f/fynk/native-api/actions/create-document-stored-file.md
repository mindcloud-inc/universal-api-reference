# Create Document Stored File with fynk

Creates a stored file for a document in fynk.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/:document/file-storage`
- **Base URL:** `https://app.fynk.com/v1/api`
- **Official documentation:** [Create Document Stored File](https://app.fynk.com/v1/docs#/operations/v1.documents.document-file-storage.store)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | path | `string` | no | Document UUID. |
| `file_name` | body | `string` | no | Stored file name. |
| `file_upload_uuid` | body | `string` | no | UUID returned by Create Document File Storage Upload URL. |
