# Check Submission Export Status with OpnForm

Retrieves submission export job status from OpnForm.

## Endpoint

- **Method:** `GET`
- **Path:** `/open/forms/:id/submissions/export/status/:jobId`
- **Base URL:** `https://api.opnform.com`
- **Official documentation:** [Check Submission Export Status](https://docs.opnform.com/api-reference/submissions/export-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The numeric ID of the form. |
| `jobId` | path | `string` | yes | The export job identifier returned by OpnForm for an asynchronous export. |
