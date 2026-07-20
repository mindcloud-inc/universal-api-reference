# Process Any Document with Eagle Doc

Creates an any-document extraction in Eagle Doc.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/anydoc/v1/processing`
- **Base URL:** `https://de.eagle-doc.com`
- **Official documentation:** [Process Any Document](https://www.eagle-doc.com/en/documentation/anydoc-ocr/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `configId` | query | `string` | no | Optional Eagle Doc custom extraction configuration ID |
| `docType` | query | `string` | no | Known Eagle Doc document type for more stable extraction |
| `file` | body | `file` | yes | Document file to upload |
| `privacy` | query | `boolean` | no | Whether Eagle Doc should avoid storing the uploaded file |
