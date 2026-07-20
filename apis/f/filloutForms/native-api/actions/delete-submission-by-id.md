# Delete Submission by ID with Fillout Forms

Deletes a submission by ID from Fillout.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/forms/:formId/submissions/:submissionId`
- **Base URL:** `https://api.fillout.com/v1/api`
- **API:** rest
- **Official documentation:** [Delete Submission by ID](https://www.fillout.com/help/api-reference/delete-submission-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form ID that owns the submission. |
| `submissionId` | path | `string` | yes | The submission ID to delete. |
