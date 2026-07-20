# Initialize Document Upload with LinkedIn

Initializes a document upload in LinkedIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/documents?action=initializeUpload`
- **Base URL:** `https://api.linkedin.com`
- **Official documentation:** [Initialize Document Upload](https://learn.microsoft.com/en-us/linkedin/marketing/community-management/shares/documents-api?view=li-lms-2026-02)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `initializeUploadRequest.owner` | body | `string` | yes | Owner URN for the member initializing the upload. |
