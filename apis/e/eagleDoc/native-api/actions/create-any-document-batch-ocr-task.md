# Create Any Document Batch OCR Task with Eagle Doc

Creates an any-document batch OCR task in Eagle Doc.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/anydoc/extract/batch/task/v1`
- **Base URL:** `https://de.eagle-doc.com`
- **Official documentation:** [Create Any Document Batch OCR Task](https://www.eagle-doc.com/en/documentation/batch-ocr/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `configId` | query | `string` | no | Optional Eagle Doc custom extraction configuration ID |
| `docType` | query | `string` | no | Known Eagle Doc document type for more stable batch extraction |
| `file` | body | `file` | yes | Archive file that contains the batch input files |
| `privacy` | query | `boolean` | no | Whether Eagle Doc should avoid storing the uploaded file |
