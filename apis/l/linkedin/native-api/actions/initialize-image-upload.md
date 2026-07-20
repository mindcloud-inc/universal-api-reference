# Initialize Image Upload with LinkedIn

Initializes an image upload in LinkedIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/images?action=initializeUpload`
- **Base URL:** `https://api.linkedin.com`
- **Official documentation:** [Initialize Image Upload](https://learn.microsoft.com/en-us/linkedin/marketing/community-management/shares/images-api?view=li-lms-2026-01)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `initializeUploadRequest.owner` | body | `string` | yes | Owner URN for the member initializing the upload. |
