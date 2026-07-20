# Get OCR Results with Natif.ai

Retrieves OCR results for a document from Natif.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/[:documentId]/ocr`
- **Base URL:** `https://api.natif.ai`
- **Official documentation:** [Get OCR Results](https://api.natif.ai/docs#/Document%20Capturing/get_ocr_documents__document_id__ocr_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | UUID of the document. |
| `include_fulltext` | query | `boolean` | no | Return page text content as a string for the natif OCR format. |
| `include_transformations` | query | `boolean` | no | Return rotation and cropping transformations. Cannot be combined with Include Fulltext. |
| `ocr_format` | query | `list` | no | Format of the returned OCR results. Accepted values: `HOCR`, `Natif`. |
