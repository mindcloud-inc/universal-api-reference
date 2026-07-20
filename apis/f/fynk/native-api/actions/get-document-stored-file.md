# Get Document Stored File with fynk

Retrieves a stored file from fynk.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/:document/file-storage/:storedFile`
- **Base URL:** `https://app.fynk.com/v1/api`
- **Official documentation:** [Get Document Stored File](https://app.fynk.com/v1/docs#/operations/v1.documents.document-file-storage.show)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | path | `string` | no | Document UUID. |
| `storedFile` | path | `string` | no | Stored file UUID. |
