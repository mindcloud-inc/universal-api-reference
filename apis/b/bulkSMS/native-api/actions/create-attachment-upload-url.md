# Create Attachment Upload URL with BulkSMS

Creates a signed BulkSMS attachment upload URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/rmm/pre-sign-attachment`
- **Base URL:** `https://api.bulksms.com/v1`
- **Official documentation:** [Create Attachment Upload URL](https://www.bulksms.com/developer/json/v1/#tag/attachments/POST/rmm/pre-sign-attachment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileExtension` | body | `string` | yes | File extension for the attachment upload, usually related to the media type. |
| `mediaType` | body | `string` | yes | Media type of the file to upload, such as application/pdf. |
