# Create Document From PDF with fynk

Creates a new document from a PDF in fynk.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/create-from-pdf`
- **Base URL:** `https://app.fynk.com/v1/api`
- **Official documentation:** [Create Document From PDF](https://app.fynk.com/v1/docs#/operations/v1.documents.create-from-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_name` | body | `string` | no | PDF file name. |
| `file_upload_uuid` | body | `string` | no | UUID returned by Create Document PDF Upload URL. |
| `initial_stage` | body | `string` | no | Initial stage for the new document. |
| `name` | body | `string` | no | Optional document name. |
