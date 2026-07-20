# Report Extraction Errors with Natif.ai

Creates an extraction error report for Natif.ai processing.

## Endpoint

- **Method:** `POST`
- **Path:** `/processing/error-reports/extractions`
- **Base URL:** `https://api.natif.ai`
- **Official documentation:** [Report Extraction Errors](https://api.natif.ai/docs#/Document%20Capturing/report_extraction_error_processing_error_reports_extractions_post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `processing_id` | body | `string` | yes | UUID of the processing request. |
| `description` | body | `string` | no | Free-text description of the extraction error. |
| `incorrect_fields[]` | body | `array<object>` | no | List of incorrect extraction fields, when known. |
