# Get Document PDF with Natif.ai

Retrieves a processed document PDF from Natif.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/[:documentId]/pdf`
- **Base URL:** `https://api.natif.ai`
- **Official documentation:** [Get Document PDF](https://api.natif.ai/docs#/Document%20Capturing/get_pdf_documents__document_id__pdf_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | UUID of the document. |
