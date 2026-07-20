# Upload Attachment with Zoho Recruit

Uploads an attachment to a Zoho Recruit record.

## Endpoint

- **Method:** `POST`
- **Path:** `/:moduleApiName/:recordId/Attachments`
- **Base URL:** `https://recruit.zoho.com/recruit/v2`
- **Official documentation:** [Upload Attachment](https://www.zoho.com/recruit/developer-guide/apiv2/upload-attachment.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `moduleApiName` | path | `string` | yes | The Zoho Recruit module API name that contains the record. |
| `recordId` | path | `string` | yes | The unique ID of the Zoho Recruit record. |
| `file` | body | `file` | no | The file to attach to the record. |
| `attachments_category` | query | `string` | no | Attachment category labels for the uploaded file. Send multiple values as a string separated by `,`. |
| `attachments_category_id` | query | `string` | no | Attachment category IDs for the uploaded file. Send multiple values as a string separated by `,`. |
| `attachmentUrl` | body | `string` | no | A publicly reachable file URL for the attachment when you are not uploading a binary file directly. |
