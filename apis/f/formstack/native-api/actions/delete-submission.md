# Delete Submission with Formstack

Permanently deletes a submission and its associated data from Formstack.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/submissions/:submissionId`
- **Base URL:** `https://www.formstack.com/api/v2025`
- **Official documentation:** [Delete Submission](https://developers.formstack.com/reference/deletesubmission-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `submissionId` | path | `number` | yes | The unique identifier of the submission to delete. |
