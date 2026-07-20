# Delete Submission with OpnForm

Deletes an existing submission from OpnForm.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/open/forms/:id/submissions/:submissionId`
- **Base URL:** `https://api.opnform.com`
- **Official documentation:** [Delete Submission](https://docs.opnform.com/api-reference/submissions/delete-submission)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The numeric ID of the form that owns the submission. |
| `submissionId` | path | `number` | yes | The numeric ID of the submission to delete. |
