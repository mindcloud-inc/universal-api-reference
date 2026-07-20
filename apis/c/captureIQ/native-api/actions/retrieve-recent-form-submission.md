# Retrieve Recent Form Submission with CaptureIQ

Retrieves a recent form submission from CaptureIQ.

## Endpoint

- **Method:** `GET`
- **Path:** `/ciq/recent-submission/v1`
- **Base URL:** `https://www.app.captureiq.ai`
- **Official documentation:** [Retrieve Recent Form Submission](https://help.captureiq.ai/api-reference/recent-submissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | query | `string` | yes | The ID of the workspace containing the form. |
| `formId` | query | `string` | yes | The ID of the form to retrieve submissions from. |
