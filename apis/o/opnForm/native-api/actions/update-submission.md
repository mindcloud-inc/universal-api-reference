# Update Submission with OpnForm

Updates an existing submission in OpnForm.

## Endpoint

- **Method:** `PUT`
- **Path:** `/open/forms/:id/submissions/:submissionId`
- **Base URL:** `https://api.opnform.com`
- **Official documentation:** [Update Submission](https://docs.opnform.com/api-reference/submissions/update-submission)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The numeric ID of the form that owns the submission. |
| `submissionId` | path | `number` | yes | The numeric ID of the submission to update. |
| `fieldValues` | body | `object` | yes | Object mapping OpnForm field IDs to the updated values for this submission. |
