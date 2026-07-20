# Send Processing Feedback with Natif.ai

Creates processing feedback for a document in Natif.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/processing/feedback/[:processingId]`
- **Base URL:** `https://api.natif.ai`
- **Official documentation:** [Send Processing Feedback](https://api.natif.ai/docs#/Document%20Capturing/report_feedback_processing_feedback__processing_id__post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `processingId` | path | `string` | yes | UUID of the processing request. |
| `description` | body | `string` | no | Free-text feedback description for annotation guidance. |
| `tag` | body | `string` | no | Optional categorization tag for training data. |
| `expected_class` | body | `string` | no | Expected document class, when known. |
| `expected_sub_documents[]` | body | `array<object>` | no | Expected sub-document split structure for splitting workflows. |
