# Get Submission by ID with Fillout Forms

Retrieves a submission by ID from Fillout.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:formId/submissions/:submissionId`
- **Base URL:** `https://api.fillout.com/v1/api`
- **API:** rest
- **Official documentation:** [Get Submission by ID](https://www.fillout.com/help/api-reference/get-submission-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form ID that owns the submission. |
| `submissionId` | path | `string` | yes | The submission ID to retrieve. |
| `includeEditLink` | query | `boolean` | no | Whether to include an edit link in the response. |
