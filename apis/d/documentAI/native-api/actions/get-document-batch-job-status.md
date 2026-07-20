# Get Document Batch Job Status with Document AI

Retrieves the status and result of a Document AI batch job.

## Endpoint

- **Method:** `GET`
- **Path:** `/document-ai/document/batch-job/batch-job/status`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Get Document Batch Job Status](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-batch-job-batch-job-status-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AsyncJobID` | query | `string` | yes | Cloudmersive async batch job ID. |
