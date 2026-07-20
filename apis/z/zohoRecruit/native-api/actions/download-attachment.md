# Download Attachment with Zoho Recruit

Retrieves an attachment from a Zoho Recruit record.

## Endpoint

- **Method:** `GET`
- **Path:** `/:moduleApiName/:recordId/Attachments/:attachmentId`
- **Base URL:** `https://recruit.zoho.com/recruit/v2`
- **Official documentation:** [Download Attachment](https://www.zoho.com/recruit/developer-guide/apiv2/download-attachments.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `moduleApiName` | path | `string` | yes | The Zoho Recruit module API name that contains the record. |
| `recordId` | path | `string` | yes | The unique ID of the Zoho Recruit record. |
| `attachmentId` | path | `string` | yes | The unique ID of the attachment. |
