# Get Submission Upload with Formstack

Retrieves an uploaded file from a Formstack submission.

## Endpoint

- **Method:** `GET`
- **Path:** `/submissions/:submissionId/upload`
- **Base URL:** `https://www.formstack.com/api/v2025`
- **Official documentation:** [Get Submission Upload](https://developers.formstack.com/reference/getsubmissionupload-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `submissionId` | path | `number` | yes | The unique identifier of the submission containing the upload. |
| `fieldId` | query | `number` | yes | The unique identifier of the field containing the uploaded file. |
| `index` | query | `number` | no | The zero-based index of the file when a field contains multiple uploads. |
