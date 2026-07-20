# Report Document Extraction Error with Natif.ai

Creates an extraction error report for a document in Natif.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/[:documentId]/error-report/extraction`
- **Base URL:** `https://api.natif.ai`
- **Official documentation:** [Report Document Extraction Error](https://api.natif.ai/docs#/Document%20Capturing/report_extraction_error_documents__document_id__error_report_extraction_post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | UUID of the document. |
| `description` | body | `string` | no | Free-text description of the extraction error. |
| `incorrect_fields[]` | body | `array<object>` | no | List of incorrect extraction fields, when known. |
