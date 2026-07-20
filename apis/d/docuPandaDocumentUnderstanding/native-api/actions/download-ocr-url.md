# Download OCR URL with DocuPanda - Document Understanding

Retrieves an OCR PDF download URL from DocuPanda.

## Endpoint

- **Method:** `GET`
- **Path:** `/document/:document_id/download/ocr-url`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Download OCR URL](https://docs.docupipe.ai/reference/download_ocr_url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | — |
| `hours` | query | `number` | no | Number of hours the URL should be valid for |
| `skip_cache` | query | `boolean` | no | Force regeneration of the OCR PDF |
