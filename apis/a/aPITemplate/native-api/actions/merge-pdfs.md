# Merge PDFs with API Template

Creates a merged PDF from multiple PDFs in API Template.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/merge-pdfs`
- **Base URL:** `https://rest.apitemplate.io`
- **Official documentation:** [Merge PDFs](https://apitemplate.io/apiv2/#tag/PDF-Manipulation-API/operation/merge-pdfs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urls[]` | body | `array<string>` | yes | URLs or data URLs of the PDFs to merge. |
| `export_type` | body | `string` | no | Return the merged PDF as JSON metadata or a file response. |
| `expiration` | body | `number` | no | Minutes before the merged PDF expires; use 0 to store permanently. |
| `cloud_storage` | body | `number` | no | Whether to upload the merged PDF to APITemplate cloud storage. |
