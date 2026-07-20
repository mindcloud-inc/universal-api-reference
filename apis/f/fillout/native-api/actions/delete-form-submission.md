# Delete Form Submission with Fillout

Deletes a form submission from Fillout.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/forms/:formId/submissions/:submissionId`
- **Base URL:** `https://api.fillout.com/v1/api`
- **Official documentation:** [Delete Form Submission](https://fillout.com/help/api-reference/delete-submission-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The public identifier of the form. |
| `submissionId` | path | `string` | yes | The identifier of the submission. |
