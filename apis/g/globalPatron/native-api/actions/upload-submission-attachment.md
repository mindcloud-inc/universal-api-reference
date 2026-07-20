# Upload Submission Attachment with Global Patron

Uploads a submission attachment to Global Patron.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/form/{formId}/submissionattachment`
- **Base URL:** `https://api.globalpatron.com`
- **Official documentation:** [Upload Submission Attachment](https://www.globalpatron.com/developers/api/submissions/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | ID of the form receiving the attachment. |
| `file` | body | `file` | yes | File to upload as a submission attachment. GlobalPatron expects the multipart field name to match a file field system name. |
