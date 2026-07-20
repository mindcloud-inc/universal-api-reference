# Initialize Video Upload with LinkedIn

Initializes a video upload in LinkedIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/videos?action=initializeUpload`
- **Base URL:** `https://api.linkedin.com`
- **Official documentation:** [Initialize Video Upload](https://learn.microsoft.com/en-us/linkedin/marketing/community-management/shares/videos-api?view=li-lms-2026-02)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `initializeUploadRequest.owner` | body | `string` | yes | Owner URN for the member initializing the upload. |
| `initializeUploadRequest.fileSizeBytes` | body | `number` | yes | — |
