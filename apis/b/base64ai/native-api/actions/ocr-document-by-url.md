# OCR Document by URL with Base64.ai

Creates an OCR result in Base64.ai from a document URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/scan`
- **Base URL:** `https://base64.ai`
- **Official documentation:** [OCR Document by URL](https://apidoc.base64.ai/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the document to OCR. |
