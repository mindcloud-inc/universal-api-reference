# Retrieve Submission Attachment with Global Patron

Retrieves a submission attachment download link from Global Patron.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/restricted/form/{formId}/submissionattachment/{attachmentId}`
- **Base URL:** `https://api.globalpatron.com`
- **Official documentation:** [Retrieve Submission Attachment](https://www.globalpatron.com/developers/api/submissions/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | ID of the form. |
| `attachmentId` | path | `string` | yes | ID of the submission attachment. |
