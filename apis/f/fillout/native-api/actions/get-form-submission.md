# Get Form Submission with Fillout

Retrieves a form submission from Fillout.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:formId/submissions/:submissionId`
- **Base URL:** `https://api.fillout.com/v1/api`
- **Official documentation:** [Get Form Submission](https://fillout.com/help/api-reference/get-submission-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The public identifier of the form. |
| `submissionId` | path | `string` | yes | The identifier of the submission. |
