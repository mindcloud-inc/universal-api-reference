# Update Submission with Global Patron

Updates a form submission in Global Patron.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/restricted/form/{formId}/submission/{submissionId}`
- **Base URL:** `https://api.globalpatron.com`
- **Official documentation:** [Update Submission](https://www.globalpatron.com/developers/api/submissions/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | ID of the form. |
| `submissionId` | path | `string` | yes | ID of the submission to update. |
| `form_fields[]` | body | `array<object>` | yes | Updated submission field values array from the GlobalPatron form definition. |
